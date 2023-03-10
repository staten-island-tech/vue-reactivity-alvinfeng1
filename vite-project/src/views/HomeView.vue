<template>
  <button @click="show = !show">Toggle</button>
  <Transition duration="550" class="button">
    <div v-if="show" class="inner">Hello</div>
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      show: true,
    };
  },
};
</script>

<style scoped></style>
