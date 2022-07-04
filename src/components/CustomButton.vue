<template>
  <div className="button-container">
    <button :disabled="disabled">{{ title }}</button>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    title: String,
    onClick: Function,
    theme: String,
    size: String,
    disabled: Boolean,
  },
})
export default class CustomInput extends Vue {
  title!: string;
  onClick!: () => void;
  theme!: "primary" | "secondary";
  size!: string;
  disabled!: boolean;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
