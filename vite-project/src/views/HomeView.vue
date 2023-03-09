<template>
  <button @click="show = !show">Toggle</button>
  <Transition duration="550" class="nested">
    <div v-if="show" class="outer">
      <div class="inner">Hello</div>
    </div>
  </Transition>
</template>

<script>
export default {};
</script>

<style scoped>
.nested .inner,
.nested .inner {
  transition: all 0.3s ease-in-out;
}

.nested .inner,
.nested .inner {
  transform: translateX(30px);
  opacity: 0;
}
</style>
