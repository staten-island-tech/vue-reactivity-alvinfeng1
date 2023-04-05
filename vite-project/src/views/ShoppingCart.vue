<template>
  <div>
    <h1>Shopping Cart</h1>
    <div v-if="cart > 0">
      <div v-for="(item, index) in cart" :key="index" class="cart-item">
        <div class="cart-item-details">
          <h2 class="name">{{ item.name }}</h2>
          <h3 class="price">${{ item.price }}</h3>
          <img class="img" :src="img" alt="" {{ item.img }}/>
        </div>
        <button @click="removeItem(index)" class="remove">Remove</button>
      </div>
      <div class="total">
        <h2>Total: ${{ getTotalPrice() }}</h2>
      </div>
    </div>
    <div v-else>
      <h2>Your cart is empty</h2>
    </div>
  </div>
</template>

<script>
import { store } from "../components/store";
export default {
  computed: {
    cart() {
      return store.cart;
    },
  },
  methods: {
    removeItem(index) {
      store.cart.splice(index, 1);
    },
    getTotalPrice() {
      let totalPrice = 0;
      store.cart.forEach((item) => (totalPrice += item.price));
      return totalPrice;
    },
  },
};
</script>

<style>
.total {
  color: chocolate;
}
.cart-item {
  border: 3px rgb(206, 206, 48) solid;
  margin: 20px auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 20%;
  background-color: wheat;
  border-radius: 10px;
}

.cart-item-details {
  display: flex;
  flex-direction: column;
}

.remove {
  height: 30px;
  width: 150px;
  background-color: rgb(232, 134, 22);
  border-radius: 10px;
  transition: all 0.3s ease;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.remove:hover {
  background-color: #f5ad11;
  transform: translateY(-3px);
}
.name {
  text-align: center;
}
.price {
  text-align: center;
}
.img {
  width: 7rem;
  min-height: 150px;
  min-width: 150px;
  border-radius: 5px;
}
</style>
