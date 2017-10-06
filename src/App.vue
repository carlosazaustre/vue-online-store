<template>
  <div id="app" class="container my-5">
    <h1>My Online Store</h1>
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
    {{ inCart }}
  </div>
</template>

<script>
import Item from './Item.vue'

export default {
  name: 'app',
  components: { Item },
  computed: {
    forSale() {
      return this.$store.getters.forSale
    },
    inCart() {
      return this.$store.getters.inCart
    }
  }
}
</script>

<style>
  /* TODO */
</style>
