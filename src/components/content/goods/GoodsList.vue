<template>
  <div class="goods">
      <goods-list-item
      v-for="item in goods" 
        :key="item.id"
        :goodsitem='item'
      ></goods-list-item>
  </div>
</template>

<script>
import GoodsListItem from './GoodsListItem'
export default {
    name:"GoodsList",
    props:{
        goods:{
            type:Array,
            default(){
                return []
            }
        }
    },
    components:{
        GoodsListItem,
    }
}
</script>

<style>
.goods{
    display: flex;
    flex-wrap: wrap;
    text-align: center;
    justify-content: space-around;
    padding: 2px;
}
</style>