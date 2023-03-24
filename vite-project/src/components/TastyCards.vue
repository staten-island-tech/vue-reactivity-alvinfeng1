<template>
  <div class="candys">
    <div class="candy">
      <h2 class="name">Name: {{ name }}</h2>
      <h3 class="price">Price: {{ price }}</h3>
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
