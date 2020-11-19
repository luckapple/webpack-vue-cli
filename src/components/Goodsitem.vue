<template>
  <div>
    <slot></slot>
    <div class="goods_item">
      <span>{{ item.title }}</span>
      <button v-if="item.del">删除</button>
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: ["item"]
};
</script>
<style scoped>
.goods_item {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  width: 20vw;
  margin: 0 auto;
}
</style>
