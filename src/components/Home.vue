<template>
  <div class="home">
    <H2>Home</H2>
    <EscenaComponent v-bind:frases="frases"></EscenaComponent>
  </div>
</template>

<script>
import EscenaComponent from './EscenaComponent.vue'

export default {
  name: 'HomeComponent',
  components: {
    EscenaComponent
  },
  data() {
    return {
      frases: [ "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",
                "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
                "L'heroi va decidir travessar la porta que el portava a casa",
                "Mentrestant, altres heroes no van tenir tanta sort en la seva elecció ..."
              ]
    }
  }
}
</script>

<style>
.home {
  background-color: yellow;
  font-weight: bold;
  padding: 10px;
}
</style>