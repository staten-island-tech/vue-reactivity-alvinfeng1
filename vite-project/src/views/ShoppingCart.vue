<template>
  <div>
    <h1>Shopping Cart</h1>
    <div v-if="cart.length > 0">
      <div v-for="(item, index) in cart" :key="index" class="cart-item">
        <div class="cart-item-details">
          <h2 class="name">{{ item.name }}</h2>
          <h3 class="price">${{ item.price }}</h3>
          <img class="img" :src="img" alt="" />
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
export default {
  name: "cart",
  props: {
    cartItems: []
  },
  methods: {
    removeItem(index) {
      this.cart.splice(index, 1);
    },
    getTotalPrice() {
      let totalPrice = 0;
      this.cart.forEach(item => totalPrice += item.price);
      return totalPrice;
    }
  }
}
</script>

<style>
.cart-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 10px;
  padding: 10px;
  border: 1px solid black;
  border-radius: 5px;
}

.cart-item-details {
  display: flex;
  flex-direction: column;
}

.remove {
  height: 30px;
  width: 100px;
  background-color: red;
  border: none; 
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