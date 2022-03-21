<template>
  <div class="escena" v-bind:style="{ backgroundImage: 'url(' + frases[currentSentence].img + ')' }">
    <!-- <h3>Escena</h3> -->
    <ul>
        <li 
          v-for="(frase, index) in frases" 
          v-bind:key="index"
          v-bind:class="{ active: index === currentSentence}">
          {{ frase.text }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'EscenaComponent',
  props: {
    frases: Array,
    currentSentence: Number
  }
}
</script>

<style scoped>
.escena {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 80vh;
}

ul {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 10px;
}

li {
  border: 2px solid rgb(25, 24, 26);
  background-color: white;
  border-radius: 25px;
  list-style: none;
  padding: 10px;
  margin-bottom: 5px;
}

.active{
  background-color: yellow;
}

</style>