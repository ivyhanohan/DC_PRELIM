<template>
    <div>
      <h1>Item List</h1>
      <Item
        v-for="item in filteredItems"
        :key="item.id"
        :item="item"
        @add-to-cart="handleAddToCart"
      />
    </div>
  </template>
  
  <script>
  import Item from './Item.vue'
  
  export default {
    name: 'ItemList',
    components: {
      Item
    },
    data() {
      return {
        items: [
          { id: 1, name: 'Item 1', price: 10, isVisible: true },
          { id: 2, name: 'Item 2', price: 20, isVisible: false },
          { id: 3, name: 'Item 3', price: 30, isVisible: true }
        ]
      }
    },
    computed: {
      filteredItems() {
        return this.items.filter(item => item.isVisible)
      }
    },
    methods: {
      handleAddToCart(item) {
        console.log(`Item added to cart: ${item.name} for $${item.price}`);
      }
    }
  }
  </script>
  