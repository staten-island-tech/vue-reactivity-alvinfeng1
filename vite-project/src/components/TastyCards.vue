<template>
  <div class="candy">
    <h2 class="name">{{ name }}</h2>
    <h3 class="price">${{ price }}</h3>
    <img class="img" :src="img" alt="" />
    <button v-on:click="" class="add">Add to Cart</button>
  </div>
</template>

<script>
import cartItems from "../views/ShoppingCart.vue";
export default {
  name: "candy",
  props: {
    name: String,
    price: Number,
    img: String,
  },
  data() {
    return {};
  },
};
</script>

<style>
.add {
  height: 30px;
  width: 150px;
  background-color: rgb(232, 134, 22);
  border-radius: 10px;
  transition: all 0.3s ease;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.add:hover {
  background-color: #f5ad11;
  transform: translateY(-3px);
}
.candy {
  border: 3px rgb(206, 206, 48) solid;
  margin: 20px auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 20%;
  background-color: wheat;
  border-radius: 10px;
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
