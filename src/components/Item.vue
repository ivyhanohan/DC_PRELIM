<template>
    <div v-if="isVisible">
      <p>Name: {{ item.name }}</p>
      <p>Price: {{ item.price }}</p>
      <button @click="addToCart">Add to Cart</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Item',
    props: {
      item: {
        type: Object,
        required: true
      }
    },
    data() {
      return {
        isVisible: true
      }
    },
    methods: {
      addToCart() {
        console.log(`Added to cart: Name - ${this.item.name}, Price - ${this.item.price}`);
        this.$emit('add-to-cart', this.item);
      }
    }
  }
  </script>
  
  <style scoped>
  /* Add some styles here if needed */
  </style>
  
