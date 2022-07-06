<template>
  <div>
    <div>
      <van-button type="info" @click="isShow = 'mobile'">{{ msg }}</van-button
      ><van-button type="primary" @click="isShow = 'email'">{{
        msg1
      }}</van-button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Vuedemoday06Login",
  props: {
    msg: {
      type: String,
    },
    msg1: {
      type: String,
      required: true,
    },
  },

  data() {
    return {
      isShow: false,
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>