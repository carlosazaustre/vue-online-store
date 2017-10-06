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
  </div>
</template>

<script>
import Item from './Item.vue'

export default {
  name: 'app',
  components: { Item },
  data () {
    return {
      forSale: [
        { invId: 1, name: 'An Item', image: '//placehold.it/200', price: 999 },
        { invId: 2, name: 'Thing', image: '//placehold.it/200', price: 1499 },
        { invId: 3, name: 'Doo-dad', image: '//placehold.it/200', price: 499 },
        { invId: 4, name: 'Other thing', image: '//placehold.it/200', price: 299 }
      ]
    }
  }
}
</script>

<style>
  /* TODO */
</style>
