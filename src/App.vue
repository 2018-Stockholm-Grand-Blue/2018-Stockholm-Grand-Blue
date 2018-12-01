<template>
  <div id="app">
      <ul id="grid" class="clear" >
          <div @click="showModal=true">
              <Hexagon v-for="job in jobs" v-bind:key="job.id"
                       v-bind:title="job.title"
                       v-bind:employer="job.employer"
                       v-bind:location="job.location"
                       v-bind:icons="job.icons"
              >
              </Hexagon>
          </div>

      </ul>
      <modal v-if="showModal" @close="showModal=false">
      </modal>
  </div>
</template>

<script>
import Hexagon from './components/Hexagon.vue'
import Modal from './components/Modal'

export default {
  name: 'app',
  components: {
    Hexagon, Modal
  },
    data: function() {
      return {
          showModal: false,
          jobs: [
              {
                  title: "DevOps Engineer",
                  employer: "ICA gruppen",
                  location: "Stockholm",
                  icons: ["fas fa-laptop", "fas fa-code"]
              },{
                  title: "Utvecklare",
                  employer: "ICA gruppen",
                  location: "Stockholm",
                  icons: ["fas fa-laptop", "fas fa-code"]
              },{
                  title: "Dataanalytiker",
                  employer: "Bravura",
                  location: "Stockholm",
                  icons: ["fas fa-laptop"]
              },
              {
                  title: "IT project manager",
                  employer: "360 Rekrytering",
                  location: "Stockholm",
                  icons: ["fas fa-laptop"]
              },{
                  title: "Android-utvecklare",
                  employer: "Dfind IT",
                  location: "Sundbyberg",
                  icons: ["fas fa-mobile-alt", "fas fa-code"]
              },
              {
                  title: "Testare",
                  employer: "Dfind IT",
                  location: "Stockholm",
                  icons: ["fas fa-laptop"]
              },
              {
                  title: "UI/UX designer",
                  employer: "i3tex",
                  location: "Stockholm",
                  icons: ["fas fa-paint-brush", "fas fa-laptop"]
              },
              {
                  title: "Junior IT-supporttekniker",
                  employer: "Bravura",
                  location: "Stockholm",
                  icons: ["fas fa-laptop", "fas fa-phone"]
              },
              {
                  title: "Tech trainee",
                  employer: "Viaplay",
                  location: "Stockholm",
                  icons: ["fas fa-laptop", "fas fa-graduation-cap"]
              },
              {
                  title: "UX trainee",
                  employer: "Nice company",
                  location: "Östermalm",
                  icons: ["fas fa-paint-brush", "fas fa-graduation-cap"]
              },
              {
                  title: "Kravanalytiker",
                  employer: "Anegy online",
                  location: "Stockholm",
                  icons: ["fas fa-laptop", "far fa-list-alt"]
              },
              {
                  title: "IT-konsult",
                  employer: "Evry",
                  location: "Stockholm",
                  icons: ["fas fa-laptop"]
              },

          ]

      }
    }
}
</script>

<style>
html {
    font-family: "Nunito", sans-serif;
}

html {
    background: #36D1DC;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #5B86E5, #36D1DC);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #5B86E5, #36D1DC); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

#app {
  font-family: 'Muli', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#grid {
    position: relative;
    width: 60%;
    margin: 0 auto;
    padding: 0; /* Clears unordered list default of 40px */
}

.clear:after {
    content: "";
    display: block;
    clear: both;
}

#grid li {
    list-style-type: none;
    position: relative;
    float: left;
    width: 27.85714285714286%;
    padding: 0 0 32.16760145166612% 0;
    -o-transform: rotate(-60deg) skewY(30deg);
    -moz-transform: rotate(-60deg) skewY(30deg);
    -webkit-transform: rotate(-60deg) skewY(30deg);
    -ms-transform: rotate(-60deg) skewY(30deg);
    transform: rotate(-60deg) skewY(30deg);
    overflow: hidden;
    visibility: hidden;
}

#grid li * {
    visibility: visible;
}

#grid li .hexagon {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: whitesmoke;
    -o-transform: skewY(-30deg) rotate(60deg);
    -moz-transform: skewY(-30deg) rotate(60deg);
    -webkit-transform: skewY(-30deg) rotate(60deg);
    -ms-transform: skewY(-30deg) rotate(60deg);
    transform: skewY(-30deg) rotate(60deg);
    overflow: hidden;
    /*background-image: url("https://placekitten.com/640/360");*/
    background-position: center center;
    background-size: cover;
}

#grid li:nth-child(3n+2) {
    margin: 0 1%;
}

#grid li:nth-child(6n+4), #grid li:nth-child(6n+5), #grid li:nth-child(6n+6) {
    margin-top: -6.9285714285%;
    margin-bottom: -6.9285714285%;
    -o-transform: translateX(50%) rotate(-60deg) skewY(30deg);
    -moz-transform: translateX(50%) rotate(-60deg) skewY(30deg);
    -webkit-transform: translateX(50%) rotate(-60deg) skewY(30deg);
    -ms-transform: translateX(50%) rotate(-60deg) skewY(30deg);
    transform: translateX(50%) rotate(-60deg) skewY(30deg);
}

#grid li:nth-child(6n+4) {
    margin-left: 0.5%;
}

#grid li .hexagon:hover {
    background-color: #E1E1E1;
    cursor: pointer;
}
</style>
