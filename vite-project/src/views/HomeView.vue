<script setup>
import TastyCards from "../components/TastyCards.vue";
export default {
  data() {
    return {
      show: true,
    };
  },
};
</script>

<template>
  <button @click="show = !show">Toggle</button>
  <Transition duration="550" class="button">
    <div v-if="show" class="inner">Hello</div>
  </Transition>
  <TastyCards />
</template>

<style>
background-color: blue;
</style>
