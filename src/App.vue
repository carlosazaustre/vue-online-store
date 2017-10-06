<template>
  <div id="app" class="container my-5">
    <div class="row mb-3">
      <div class="col-md-9">
        <h1>My Online Store</h1>
      </div>
      <div class="col-md-3">
        <shopping-cart></shopping-cart>
      </div>
    </div>
    <div class="row">
      <item
        v-for="item in forSale"
        :key="item.invId"
        :invId="item.invId"
        :image="item.image"
        :name="item.name"
        :price="item.price"
      ></item>  
    </div>
  </div>
</template>

<script>
import Item from './Item.vue'
import ShoppingCart from './ShoppingCart.vue'

export default {
  name: 'app',
  components: { Item, ShoppingCart },
  computed: {
    forSale() {
      return this.$store.getters.forSale
    }
  }
}
</script>

<style>
  /* TODO */
</style>
