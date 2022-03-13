<template>
  <div class="escena">
    <H3>Escena</H3>
     <ul>
        <li v-for="(frase, index) in frases" v-bind:key="index">{{frase}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'EscenaComponent',
  props: {
    frases: Array
  }
}
</script>

<style>
.escena {
  background-color: greenyellow;
}
</style>