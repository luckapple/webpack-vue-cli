<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <hr />
    <GoodsList :list="list" />
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";
import GoodsList from "@/components/GoodsList";

export default {
  components: {
    HelloWorld,
    GoodsList
  },
  data() {
    return {
      list: [
        {
          name: "语文",
          title: "课程一",
          teacher: "康熙",
          del: false
        },
        {
          name: "数学",
          title: "课程二",
          teacher: "乾隆",
          del: true
        },
        {
          name: "英语",
          title: "课程三",
          teacher: "雍正",
          del: false
        }
      ]
    };
  }
};
</script>
