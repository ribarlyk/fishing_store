<template>
  <div class="cart-container">
    <span>{{ products }} продукти - {{ price }} лева</span>
    <nuxt-icon name="cart" class="cart-icon" />
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const products = ref(0);
const price = ref(0);
</script>

<style scoped>
.cart-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 20px;
}
.cart-icon {
  font-size: 2rem;
  margin-left: 0.7rem;
}
.menu-item,
.cart-container {
  transition: color 0.3s;
  color: #fff;
}
.cart-container:hover {
  color: #e2bd36;
  cursor: pointer;
}
</style>
