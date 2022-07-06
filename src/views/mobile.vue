<template>
  <div>
    <div class="login-mobile">
      <span>选择所在地区(实名认证主题所在地)</span>
      <van-icon name="question-o" />
    </div>
    <div class="adress-mobile">
      <van-radio-group v-model="radio" direction="horizontal">
        <van-radio name="1">中国大陆</van-radio>
        <van-radio name="2">中国香港</van-radio>
      </van-radio-group>
    </div>
    <div class="user-info-mobile">
      <div>手机号码</div>
      <!-- 输入手机号，调起手机号键盘 -->
      <van-field v-model="tel" type="tel" placeholder="手机号" class="msg" />
      <van-field
        v-model="sms"
        center
        clearable
        placeholder="请输入短信验证码"
        border
        input-align="left"
        class="msg"
      >
        <template #button>
          <van-button size="small" type="primary">发送验证码</van-button>
        </template>
      </van-field>
    </div>
    <div class="user-password-mobile">
      <div>登录密码</div>
      <!-- 输入密码 -->
      <van-field
        v-model="password"
        type="password"
        placeholder="密码"
        class="msg"
      />
      <!-- 输入密码 -->
      <van-field
        v-model="aginPassword"
        type="password"
        placeholder="确认密码"
        class="msg"
      />
    </div>
    <div>
      <div>邀请码(选填)</div>
      <!-- 输入任意文本 -->
      <van-field v-model="text" placeholder="输入客户经理邀请码" class="msg" />
    </div>
  </div>
</template>

<script>
// import phonePannel from "@/components/phone-pannel.vue";
export default {
  //   components: {
  //     phonePannel,
  //   },
  props: {},
  name: "Vuedemoday06Mobile",

  data() {
    return {
      radio: "1",
      tel: "",
      sms: "",
      password: "",
      aginPassword: "",
      text: "",
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style scoped>
.adress-mobile {
  margin-top: 20px;
  margin-bottom: 20px;
}
.msg {
  border-bottom: 2px solid black;
  height: 40px;
  border-radius: 2px;
  margin: 10px 0;
}
</style>