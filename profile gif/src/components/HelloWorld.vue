<template>
  <div class="hello">
    <div id="demo">
      <div id="inner-demo">
        <h1 id="inner-demo-2">Hi There</h1>
      </div>
    </div>
    <VueParticle domId="demo" :config="particleConfig"/>
  </div>
</template>

<script>
import VueParticle from "vue-particlejs";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    VueParticle
  },
  data() {
    return {
      particleConfig: {
        particles: {
          number: { value: 150, density: { enable: true, value_area: 800 } },
          color: { value: "#000000" },
          shape: {
            type: "circle",
            stroke: { width: 0, color: "#000000" },
            polygon: { nb_sides: 5 },
            image: { src: "img/github.svg", width: 100, height: 100 }
          },
          opacity: {
            value: 0.5,
            random: false,
            anim: { enable: false, speed: 1, opacity_min: 0.1, sync: false }
          },
          size: {
            value: 3,
            random: true,
            anim: { enable: false, speed: 40, size_min: 0.1, sync: false }
          },
          line_linked: {
            enable: true,
            distance: 150,
            color: "#555555",
            opacity: 0.4,
            width: 1
          },
          move: {
            enable: true,
            speed: 6,
            direction: "none",
            random: false,
            straight: false,
            out_mode: "out",
            bounce: false,
            attract: { enable: false, rotateX: 600, rotateY: 1200 }
          }
        },
        interactivity: {
          detect_on: "canvas",
          events: {
            onhover: { enable: false, mode: "repulse" },
            onclick: { enable: false, mode: "push" },
            resize: true
          },
          modes: {
            grab: { distance: 400, line_linked: { opacity: 1 } },
            bubble: {
              distance: 400,
              size: 40,
              duration: 2,
              opacity: 8,
              speed: 3
            },
            repulse: { distance: 200, duration: 0.4 },
            push: { particles_nb: 4 },
            remove: { particles_nb: 2 }
          }
        },
        retina_detect: true
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#demo {
  width: 100%;
  height: 50vh;
  background: url("") white;
}
#inner-demo {
  width: 100%;
  height: 0%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: black;
  font-size: 2em;
}
#inner-demo h1 {
  position: relative;
  top: 4em;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #888888;
}
</style>
