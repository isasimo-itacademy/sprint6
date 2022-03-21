<template>
  <div class="home">
    <!-- <h1>Home</h1> -->
    <div v-if="showScene">
      <BotonsComponent :currentSentence="currentSentence" @mostra-seguent="incrementa" @mostra-anterior="resta"/>
      <EscenaComponent :frases="frases" :currentSentence="currentSentence"></EscenaComponent>
    </div>
    <div v-else>
      <button @click="showScene = !showScene">Començar</button>
    </div>
  </div>
</template>

<script>
import EscenaComponent from './EscenaComponent.vue'
import BotonsComponent from './BotonsComponent.vue'

export default {
  name: 'HomeComponent',
  components: {
    EscenaComponent,
    BotonsComponent
  },
  data() {
    return {
      frases: [ { 
                  text: "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",
                  img: require('../assets/1.jpg')
                },
                { 
                  text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
                  img: require('../assets/2.jpg')
                },
                { 
                  text: "L'heroi va decidir travessar la porta que el portava a casa",
                  img: require('../assets/3.jpg')
                },
                { 
                  text: "Mentrestant, altres heroes no van tenir tanta sort en la seva elecció ...",
                  img: require('../assets/4.jpg')
                }
              ],
      currentSentence: 0,
      showScene: false
    }
  },
  methods: {
    incrementa() {
        if (this.currentSentence < (this.frases.length - 1)) {
            this.currentSentence++;
        } else {
            this.currentSentence = 0;
        }
    },
    resta() {
        if (this.currentSentence > 0) {
            this.currentSentence--;
        } else {
            this.currentSentence = (this.frases.length - 1);
        }
    }
  }
}
</script>

<style>
.home {
  background-color: rgb(225 236 249);
  font-weight: bold;
  padding: 10px;
}
</style>