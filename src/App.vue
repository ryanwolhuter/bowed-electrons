<template>
  <Particles id="tsparticles" :options="particlesOptions" />
  <Slide>
    <h1>Toolset for the Internet of Musical Things</h1>
  </Slide>
  <Slide>
    <h1>Motivations</h1>
  </Slide>
  <Slide>
    <h2>Synchronization in Musical Performance</h2>
    <div class="synchro__body">
      <div class="synchro__text">
        <p>How do we coordinate live musical performances?</p>
        <p>
          We use a wireless, analogue communication device:
          <strong>the stick</strong>.
        </p>
        <p>
          The conductor can't control the musicians directly; she can only send
          messages.
        </p>
        <p>
          We can learn from the effectiveness of the stick for controlling
          digital music performances.
        </p>
      </div>
      <img src="./assets/conductor.gif" />
    </div>
  </Slide>
  <Slide>
    <h1>Message Passing In Music</h1>
  </Slide>
  <Slide>
    <h2>What is a Distributed System?</h2>
    <p>
      A system whose components are located on separate computers. 
    </p>
    <p>These computers are usually physically separate, sometimes over huge distances.</p>
    <p>These components communicate by passing messages.</p>
    <h3>Benefits</h3>
    <div class="distributed">
      <ul>
        <li>Scalable</li>
        <li>Reliable (fault-tolerant)</li>
        <li>Efficient (concurrent)</li>
      </ul>
      <img src="./assets/distributed.png" class="distributed" />    </div>
  </Slide>
  <Slide>
    <h1>Joe Armstrong</h1>
    <img src="./assets/joe_armstrong.jpg" />
    <img src="./assets/joe_armstrong.png" />
  </Slide>
  <Slide>
    <h2>Open Sound Control</h2>
    <p>
      Open Sound Control (OSC) is a communication protocol for sending
      information across a computer network. It can facilitate messages among
      computers, synthesizers, and other multimedia devices.
    </p>

    <p>
      OSC is the lifeblood of SuperCollider, managing the communication between
      the server and the application language.
    </p>

    <p>
      OSC messages are can take advantage of established net transmission
      protocols.
    </p>
  </Slide>
  <Slide>
    <h2>Areas of Application</h2>
    <ul>
      <li>Music, video, lighting control</li>
      <li>Sensor/gesture-based electronic musical instruments</li>
      <li>Mapping non-musical data to sound parameters (Sonification)</li>
      <li>Controlling any electronic device</li>
      <li>Networked LAN musical performances</li>
    </ul>
  </Slide>
  <Slide>
    <h2>Common Misconceptions about OSC and MIDI</h2>
    <ul>
      <li>
        OSC can only be used with UDP - OSC can actually be used with any
        transmission protocol.
      </li>
      <li>Has to be on same device-</li>
      <li>Message passing isn’t guaranteed with OSC -</li>
      <li>
        Message passing is guaranteed with MIDI - MIDI protocol has no way of
        knowing if messages are being received (an example is the common “Note
        off” problem)
      </li>
      <li>
        MIDI is faster than OSC- OSC has been proven to be much faster than
        MIDI, both through cables and across networks.
      </li>
    </ul>
  </Slide>
  <Slide>
    <h1>How to Send OSC Messages</h1>
    <p>(The SuperCollider way)</p>
  </Slide>
  <Slide>
    <h1>Erlang? Never heard of it</h1>
  </Slide>
  <Slide>
    <h1>What is Elixir?</h1>
  </Slide>
  <Slide>
    <h1>Elixir and the Internet of Things</h1>
    <p>Phoenix?</p>
    <p>Nerves?</p>
    <p>Membrane?</p>
  </Slide>
  <Slide>
    <h2>The Internet of Musical Things</h2>
    <p>
      Musical Thing defined as “a computing device capable of sensing,
      acquiring, processing, or actuating, and exchanging data serving a musical
      purpose”.
    </p>
    <p>
      IoMusT is then the ensemble of interfaces, data and protocols that enable
      interactions between humans and Musical Things or between Musical Things
      themselves for composition or participatory performance.
    </p>
  </Slide>
  <Slide>
    <h2>"Issues" with the Internet of Musical Things</h2>
    <h3>(and how Elixir can solve them)</h3>
  </Slide>
  <Slide>
    <h1>Implementation Details</h1>
  </Slide>
  <Slide>
    <h2>Anthropogenic Soundscapes for IoMusT</h2>
    <p>
      Creating a distributed network through Elixir and OSC laid the foundations
      for our ongoing interdisciplinary research project. We are creating a
      distributed instrument for an audio-visual composition.
    </p>
    <p>
      The music will be a soundscape of a collage of ‘sound slides’ from
      electro-magnetic radiation recordings and melodies played by SuperCollider
      on instruments synthesised through the network.
    </p>
    <p>
      The project will culminate in a performance and then be stored on a
      website with code for other musicians who may be interested in similar
      projects.
    </p>
    <p>
      The inspiration for the musical elements of the composition came from the
      Martin Rumori installation “Promenade, Anecdote” wherein he explored the
      concepts of ‘anecdotal music’ and ‘Klangias’ (everyday sound recordings
      that anyone could take, as they would take holiday pictures).
    </p>
  </Slide>
  <Slide>
    <h2>Future Projects with this Toolset</h2>
    <ul>
      <li>
        Composition using simultaneously without overloading one computer.
      </li>

      <li>
        Worldwide real-time collaboration of electronic musicians, dj’s, visual
        artists and live coders.
      </li>

      <li>Synchronised performance events in different countries.</li>

      <li>
        Distributed Systems for computationally heavy elements (like AI
        composition or heavy synthesis algorithms) being calculated on a
        separate machine so that your computer can just focus on generating the
        music.
      </li>
    </ul>
  </Slide>
  <Slide>
    <h1>Toolset</h1>
    <ul>
      <li>Open Sound Control (OSC)</li>
      <li>Elixir</li>
      <li>WebRTC</li>
    </ul>
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
      pauseOnOutsideViewport: true,
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
        move: {
          direction: 'top',
          enable: true,
          outMode: 'destroy',
          random: false,
          speed: 1,
          straight: false,
        },
        number: {
          density: {
            enable: true,
            value_area: 800,
          },
          value: 10,
        },
        opacity: {
          value: 1,
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
  height: 1500vh;
}

h1 {
  font-size: 5rem;
  max-width: 800px;
  margin: 1rem;
}

h2 {
  font-size: 3rem;
  max-width: 800px;
  margin: 1rem;
}

h3 {
  font-size: 2rem;
  margin-top: 2rem;
  margin-left: 1rem;
}

p,
li {
  font-size: 1.4rem;
  max-width: 800px;
  margin: 1.5rem;
}

img {
  margin: 2rem;
  border-radius: 1rem;
}

img.distributed {
  width: 400px;
}

div.distributed {
  display: flex;
  align-items: center;
}

.synchro__body {
  display: flex;
  align-items: center;
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
