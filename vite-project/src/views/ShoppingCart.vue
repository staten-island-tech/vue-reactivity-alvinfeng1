<script>
export default {
  data() {
    return {
      cartItems: [],
    };
  },
};
</script>

<template>
  <h1>Shopping Cart</h1>
  <div class="Cart-Container"></div>
</template>

<style>
h1 {
  text-align: center;
}
.Cart-Container {
  width: 70%;
  height: 85%;
  background-color: rgba(166, 110, 6, 0.972);
  border-radius: 20px;
  box-shadow: 0px 25px 40px #1687d933;
}
</style>
