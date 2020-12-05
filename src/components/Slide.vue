<template>
  <div class="slide">
    <Particles id="tsparticles" :options="particlesOptions" />
    <section class="content">
      <div class="text">
        <slot></slot>
      </div>
    </section>
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
  display: grid;
  align-items: center;
  justify-content: center;
}

.content {
  width: 80vw;
  height: 80vh;
  padding: 4rem;
  background: hsla(0, 100%, 100%, 0.5);
  border-radius: 1rem;
  backdrop-filter: blur(5px);

  display: grid;
  align-items: center;
  justify-content: center;
}
</style>