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
    <p>A system whose components are located on separate computers.</p>
    <p>
      These computers are usually physically separate, sometimes over huge
      distances.
    </p>
    <p>These components communicate by passing messages.</p>
    <h3>Benefits</h3>
    <div class="distributed">
      <ul>
        <li>Scalable</li>
        <li>Reliable (fault-tolerant)</li>
        <li>Efficient (concurrent)</li>
      </ul>
      <img src="./assets/distributed.png" class="distributed" />
    </div>
  </Slide>
  <Slide>
    <h1>Joe Armstrong</h1>
    <img src="./assets/joe_armstrong.jpg" />
    <img src="./assets/joe_armstrong.png" />
  </Slide>
  <Slide>
    <h2>Open Sound Control</h2>
    <p>
      Open Sound Control (OSC) is a protocol for communication among computers.
    </p>

    <p>
      It can facilitate messages among computers, synthesizers, and other
      multimedia devices.
    </p>

    <p>
      OSC is not limited to controlling audio devices, it can control anything.
    </p>

    <p>It is optimized for modern networking technology.</p>

    <p>
      OSC is an integral part SuperCollider, where it is used to facilitate
      communication between the server and the sound engine.
    </p>
  </Slide>
  <Slide>
    <h2>Areas of Application</h2>
    <ul>
      <li>Music, video, and lighting control</li>
      <li>Sensor/gesture-based electronic musical instruments</li>
      <li>Mapping non-musical data to sound parameters (sonification)</li>
      <li>Networked musical performances</li>
    </ul>
  </Slide>
  <Slide>
    <table>
      <thead>
        <tr>
          <th scope="col"></th>
          <th scope="col">OSC</th>
          <th scope="col">MIDI</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Message Types</th>
          <td>
            Human readable <br />
            User defined
          </td>
          <td>
            Byte-encoded <br />
            Pre-determined
          </td>
        </tr>
        <tr>
          <th scope="row">Formats</th>
          <td>
            Numbers, text, colors (RGBA), <br />
            even MIDI
          </td>
          <td>1-byte integers (0-127)</td>
        </tr>
        <tr>
          <th scope="row">Time-tagging</th>
          <td>Yes</td>
          <td>No</td>
        </tr>
        <tr>
          <th scope="row">Transport</th>
          <td>LAN and Internet (UDP, TCP, WebSockets, WebRTC)</td>
          <td>Cable-based transfer</td>
        </tr>
        <tr>
          <th scope="row">Number of Channels</th>
          <td>Unlimited</td>
          <td>16</td>
        </tr>
        <tr>
          <th scope="row">Transfer Speed</th>
          <td>Gigabit</td>
          <td>31,250 bits / second</td>
        </tr>
      </tbody>
    </table>
  </Slide>
  <Slide>
    <h2>Common Misconceptions about OSC and MIDI</h2>
    <ul>
      <li>OSC can only be used with UDP.</li>
      <li>OSC can only be used by applications on the same device.</li>
      <li>Message passing is guaranteed with MIDI.</li>
      <li>MIDI is faster than OSC.</li>
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
      Musical Things are devices capable of sensing, processing, and exchanging
      data for musical purposes.
    </p>
    <p>
      IoMusT is the ensemble of interfaces, data and protocols that enable
      interactions between humans and Musical Things.
    </p>
  </Slide>
  <Slide>
    <h2>"Challenges"</h2>
    <p>(and how Elixir can solve them)</p>
    <ul>
      <li><em>The IoMusT Ontology (Web Semantics)</em></li>
      <li><em>IoMusT: Vision and Challenges (IEEE)</em></li>
    </ul>
    <p>
      "For musical applications the latency must be in the order of
      milliseconds"
    </p>

    <p>"The synchronization of audio streams produced by devices that don't share the same clock."</p>

    <p>"Even if devices initially share the same clock, they need a re-synchronization procedure from time to time."</p>

    <p>"There are many different audio and visual file formats."</p>
  </Slide>
  <Slide>
    <img src="./assets/server.png" class="server" />
  </Slide>
  <Slide>
    <h2>Research Project</h2>
    <p>A distributed instrument for an audio-visual composition.</p>
    <p>
      The composition, <em>Anthropogenic Soundscapes for IoMusT</em>, will be a
      collage of "sound slides" from electro-magnetic radiation recordings and
      melodies played by SuperCollider.
    </p>
    <p>
      Our project is open source, and we are inviting other musicians and coders
      to join us.
    </p>
  </Slide>
  <Slide>
    <h2>Future Projects</h2>
    <ul>
      <li>
        Composition with many music programs simultaneously.
      </li>

      <li>
        Worldwide real-time collaboration of electronic musicians, DJs, visual artists and live coders.
      </li>

      <li>Synchronized performances in different countries.</li>

      <li>
        Distributing computationally heavy composition and synthesis tasks across multiple machines.
      </li>
    </ul>
  </Slide>
  <Slide>
    <h1>IoMusT Toolset</h1>
    <ul>
      <li>Open Sound Control (OSC)</li>
      <li>Elixir</li>
      <li>Phoenix</li>
      <li>Nerves</li>
      <li>Membrane</li>
      <li>Raspberry Pi and Beagleboard</li>
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
  height: 1000vh;
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

ul {
  list-style: circle;
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

img.server {
  width: 100%;
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

table {
  table-layout: fixed;
  width: 100%;
  border-collapse: collapse;
  border: 2px solid white;
  border-radius: 1rem;
}

th,
td {
  padding: 0.5rem;
  border: 2px solid white;
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
