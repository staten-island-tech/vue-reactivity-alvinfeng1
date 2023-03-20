<template>
  <button @click="show = !show">Toggle</button>
  <Transition duration="550" class="button">
    <div v-if="show" class="inner">Hello</div>
  </Transition>
  <TastyCards />
</template>

<script setup>
export default {
  data() {
    return {
      show: true,
    };
  },
};
</script>

<style>
background-color: blue;
</style>
