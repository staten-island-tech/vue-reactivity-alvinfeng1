<template>
  <candy
    v-for="item in store.cart"
    :name="item.name"
    :price="item.price"
    :img="item.img"
  ></candy>
  <button @click="removeItem(index)" class="remove">Remove</button>
  <div class="total">
    <h2>Total: ${{ getTotalPrice() }}</h2>
  </div>
</template>

<script>
import { store } from "../components/store";
export default {
  data() {
    return {
      store,
    };
  },
  computed: {
    cart() {
      return store.cart;
    },

    getImage: function () {
      return this.image;
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
  components: {
    candy,
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
