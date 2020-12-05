<template>
  <div class="slide">
    <Particles id="tsparticles" :options="particlesOptions" />
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Slide',
  data() {
    return {
      particlesOptions: {
      fpsLimit: 60,
      particles: {
        color: {
          value: '#000000',
        },
        links: {
          color: '#000000',
          distance: 150,
          enable: true,
          opacity: 0.5,
          width: 1,
        },
        collisions: {
          enable: true,
        },
        move: {
          direction: 'none',
          enable: true,
          outMode: 'bounce',
          random: false,
          speed: 6,
          straight: false,
        },
        number: {
          density: {
            enable: true,
            value_area: 800,
          },
          value: 20,
        },
        opacity: {
          value: 0.5,
        },
        shape: {
          type: 'circle',
        },
        size: {
          random: true,
          value: 5,
        },
      },
      detectRetina: true,
    }
    }
  }
}
</script>

<style scoped>
#tsparticles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
}
.slide {
  height: 100vh;
}
</style>