<template>
  <div>
    <table border="1">
      <thead>
        <tr>
          <th>序号</th>
          <th>姓名</th>
          <th>年龄</th>
          <th>头像</th>
        </tr>
      </thead>
      <thead>
        <tr v-for="(item, index) in arr" :key="index">
          <td>
            <slot name="index" :row="index">{{ index }}</slot>
          </td>
          <td>
            <slot name="name" :row="item">{{ item.name }}</slot>
          </td>
          <td>
            <slot name="age" :row="item">{{ item.age }}</slot>
          </td>
          <td v-if="type == 0">
            <slot name="img" :row="item">
              <img :src="item.headImgUrl" alt="" />
            </slot>
          </td>
          <td v-else-if="type == 1">
            <slot name="img" :row="item">
              <a href="item.headImgUrl">{{ item.headImgUrl }}</a>
            </slot>
          </td>
          <td v-else>
            <slot name="img" :row="item">
              {{ item.headImgUrl }}
            </slot>
          </td>
        </tr>
      </thead>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    arr: {
      type: Array,
    },
    type: {
      type: String,
    },
  },

  data() {
    return {};
  },
};
</script>