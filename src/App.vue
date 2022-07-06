<template>
  <div>
    <UserTable :arr="list" type="2">
      <template #index="scope">{{ scope.row + 1 }}</template>
      <template #name="scope">{{ scope.row.name }}</template>
      <template #age="scope"
        ><input type="text" v-model="scope.row.age"
      /></template>
      <template #img></template>
    </UserTable>
  </div>
</template>

<script>
import UserTable from "./views/UserTable.vue";
export default {
  components: {
    UserTable,
  },
  name: "Vuedemoday06App",

  data() {
    return {
      list: [
        {
          name: "小传同学",
          age: 18,
          headImgUrl:
            "http://yun.itheima.com/Upload/./Images/20210303/603f2d2153241.jpg",
        },
        {
          name: "小黑同学",
          age: 25,
          headImgUrl:
            "http://yun.itheima.com/Upload/./Images/20210304/6040b101a18ef.jpg",
        },
        {
          name: "智慧同学",
          age: 21,
          headImgUrl:
            "http://yun.itheima.com/Upload/./Images/20210302/603e0142e535f.jpg",
        },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>