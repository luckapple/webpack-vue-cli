<template>
  <div>
    <Slots>
      <template v-slot:header>
        <div>顶部s</div>
      </template>
      <template>
        <div>内容s</div>
      </template>
      <template v-slot:footer>
        <div>底部s</div>
      </template>
    </Slots>
    <div v-for="(item, index) in list" :key="index">
      <div class="goods_list">
        <b style="color:red">{{ item.name }}</b>
        <Goodsitem :item="item"> </Goodsitem>
        <b style="color:red">{{ item.teacher }}</b>
      </div>
      <hr />
    </div>
  </div>
</template>

<script>
import Goodsitem from "@/components/Goodsitem";
import Slots from "@/components/Slots";
export default {
  props: ["list"],
  components: { Goodsitem, Slots }
};
</script>
<style scoped>
.goods_list {
  width: 30vw;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
