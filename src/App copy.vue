<template>
  <div class="login">
    <login msg1="邮箱登录" msg="手机登录"></login>
    <div class="components">
      <keep-alive> <component :is="isShow"></component></keep-alive>
    </div>
  </div>
</template>

<script>
import login from "./components/login.vue";
import email from "@/views/email.vue";
import mobile from "@/views/mobile.vue";
export default {
  components: {
    email,
    mobile,
    login,
  },
  name: "Vuedemoday06App",

  data() {
    return {
      isShow: "email",
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style  scoped>
.login {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 60px;
  padding: 0 40px;
}
.components {
  margin-top: 20px;
}
</style>