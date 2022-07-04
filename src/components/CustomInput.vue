<template>
  <div className="input-container">
    <label>{{ label }}</label>
    <input
      :placeholder="placeholder"
      :value="value"
      :onChange="onChange"
      class="input-field"
    />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    value: String,
    onChange: Function,
    label: String,
    placeholder: String,
  },
})
export default class CustomInput extends Vue {
  value!: string;
  onChange!: () => void;
  label!: string;
  placeholder!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.input-container {
  height: 60px;
  display: flex;
  flex-direction: column;
  align-items: space-between;
  justify-content: space-between;
  margin-top: 20px;
  margin-bottom: 20px;
}
.input-field {
  height: 30px;
  width: 200px;
  border-radius: 5px;
  border: solid 1px;
  padding: 10px;
  font-size: 15px;
  outline: none;
}
</style>
