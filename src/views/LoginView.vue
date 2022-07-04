<template>
  <div class="login-signup-container">
    <CustomInput :value="email" label="Email" placeholder="Enter Email" />
    <CustomInput
      :value="password"
      label="Enter Password"
      placeholder="Enter Password"
    />
    <CustomButton :disabled="true" title="Submit" />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import CustomInput from "@/components/CustomInput.vue";
import CustomButton from "@/components/CustomButton.vue";

@Options({
  components: {
    CustomInput,
    CustomButton,
  },
  data() {
    return {
      email: "",
      password: "",
    };
  },
})
export default class LoginView extends Vue {}
</script>

<style scoped lang="scss">
.login-signup-container {
  display: flex;
  margin-top: 8%;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
