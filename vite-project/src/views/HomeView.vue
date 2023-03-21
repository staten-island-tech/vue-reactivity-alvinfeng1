<script>
export default {
  data() {
    return {
      show: true,
    };
  },
};
import TastyCards from ./components/TastyCards.vue
</script>

<template>
  <button @click="show = !show">Toggle</button>
  <Transition duration="550" class="button">
    <div v-if="show" class="inner">Hello</div>
  </Transition>
</template>

<style>
background-color: blue;
</style>
