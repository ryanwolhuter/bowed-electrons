<template>
  <Slide>
    <h1>Heading</h1>
    <p>Text</p>
  </Slide>
</template>

<script>
  import Slide from '@/components/Slide.vue'


export default {
  name: 'App',
  components: {
    Slide
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: teal;
  color: #ffffff;
}

* {
  margin: 0;
  padding: 0;
  overflow: hidden;
  box-sizing: border-box;
}
</style>
