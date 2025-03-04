<template>
    <div>
      <CartTitle :username="username"></CartTitle>
      <div class="cart-container">
        <CartList
          class="cart-list"
          :cart-items="shoppingCartItems"
          @item-remove="removeItem($event)"
          @quantity-update="updateQuantity($event)"
        ></CartList>
        <OrderSummary
          class="order-summary"
          :cart-items="shoppingCartItems"
        ></OrderSummary>
      </div>
    </div>
  </template>
  
  <script setup>
  import CartTitle from '@/components/CartTitle.vue'
  import CartList from '@/components/CartList.vue'
  import OrderSummary from '@/components/OrderSummary.vue'
  </script>
  
  <style scoped>
  /* Styles for the cart list and order summary */
  .cart-container {
    display: flex;
    align-items: flex-start;
    max-width: 1200px;
    margin: auto;
  }
  
  .cart-list {
    flex-grow: 2;
    margin-right: 20px;
  }
  
  .order-summary {
    flex-basis: 300px;
    background-color: #f9fafb;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  </style>