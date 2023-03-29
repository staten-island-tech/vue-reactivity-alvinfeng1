<template>
  <div class="candys">
    <div class="candy">
      <h2 class="name">{{ name }}</h2>
      <h3 class="price">${{ price }}</h3>
      <img class="img" :src="img" alt="" />
      <button class="add">Add to Cart</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "candy",
  props: {
    name: String,
    price: Number,
    img: String,
  },
};
</script>

<style>
.candys {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
}
.candy {
  border: 3px rgb(206, 206, 48) solid;
  margin: 20px auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 20%;
  background-color: white;
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
}
</style>
