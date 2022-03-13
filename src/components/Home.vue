<template>
  <div class="home">
    <h1>Home</h1>
    <BotonsComponent :currentSentence="currentSentence" @mostra-seguent="incrementa" @mostra-anterior="resta"/>
    <EscenaComponent :frases="frases" :currentSentence="currentSentence"></EscenaComponent>
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
      frases: [ "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",
                "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
                "L'heroi va decidir travessar la porta que el portava a casa",
                "Mentrestant, altres heroes no van tenir tanta sort en la seva elecció ..."
              ],
      currentSentence: 0
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
  background-color: #a6b7c5;
  font-weight: bold;
  padding: 10px;
}
</style>