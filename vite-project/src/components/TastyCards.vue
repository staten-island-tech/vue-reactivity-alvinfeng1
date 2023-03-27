<template>
  <div class="candys">
    <div class="candy">
      <h2 class="name">{{ name }}</h2>
      <h3 class="price">${{ price }}</h3>
      <img class="img" :src="img" alt="" />
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
  max-width: 30%;
  flex-wrap: wrap;
  justify-content: space-between;
}
.candy {
  border: 3px rgb(206, 206, 48) solid;
  margin: 20px auto;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-items: center;
}
.name {
  text-align: center;
}
.price {
  text-align: center;
}
.img {
  width: 7rem;
}
</style>
