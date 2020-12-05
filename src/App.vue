<template>
  <!-- <Particles id="tsparticles" :options="particlesOptions" /> -->
  <Slide>
    <h1>Toolset for the Internet of Musical Things</h1>
  </Slide>
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
  },
  data() {
    return {
      particlesOptions: {
      fpsLimit: 60,
      particles: {
        color: {
          value: '#ffffff',
        },
        links: {
          color: '#ffffff',
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

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: teal;
  color: #ffffff;
  height: fit-content;
}

* {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  box-sizing: border-box;
  scrollbar-width: thin;
  scrollbar-color: transparent transparent;
}

#tsparticles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 200vh;
}

h1 {
  font-size: 5rem;
  max-width: 800px;
}

/* Works on Chrome/Edge/Safari */
*::-webkit-scrollbar {
  width: 0px;
}
*::-webkit-scrollbar-track {
  background: transparent;
}
*::-webkit-scrollbar-thumb {
  background-color: transparent;
  border-radius: 20px;
  border: 3px solid transparent;
}
</style>
