<template>
  <div>
    <div class="user-info-mobile">
      <div>手机号码</div>
      <!-- 输入手机号，调起手机号键盘 -->
      <slot name="mobile"
        ><van-field
          v-model="tel"
          type="text"
          class="msg"
          placeholder="请输入手机号"
      /></slot>
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
  </div>
</template>

<script>
export default {
  name: "Vuedemoday06MobileCom",

  data() {
    return {
      tel: "",
      sms: "",
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>