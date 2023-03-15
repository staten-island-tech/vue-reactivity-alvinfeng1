<template>
  <button @click="show = !show">Toggle</button>
  <Transition duration="550" class="button">
    <div v-if="show" class="inner">Hello</div>
  </Transition>
  <newfood />
</template>

<script>
export default {
  data() {
    return {
      show: true,
    };
  },
};
import newfood from "../components/cards.vue";
</script>

<style scoped></style>
