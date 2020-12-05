<template>
  <div class="slide">
    <section class="content">
      <div class="text">
        <slot></slot>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Slide'
}
</script>

<style scoped>
.slide {
  height: 100vh;
  display: grid;
  align-items: center;
  justify-content: center;
}

.content {
  width: 80vw;
  height: 80vh;
  padding: 4rem;
  background: hsla(173, 10%, 83%, 0.5);
  border-radius: 1rem;
  backdrop-filter: blur(5px);

  display: grid;
  align-items: center;
  justify-content: center;
}
</style>