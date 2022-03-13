<template>
  <div class="escena">
    <h3>Escena</h3>
    <ul>
        <li 
          v-for="(frase, index) in frases" 
          v-bind:key="index"
          v-bind:class="{ active: index === currentSentence}">
          {{frase}}
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
  background-color: rgb(225 236 249);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

ul {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 10px;
}

li {
  border: 2px solid rgb(25, 24, 26);
  border-radius: 25px;
  list-style: none;
  padding: 10px;
  margin-bottom: 5px;
}

.active{
  background-color: yellow;
}

</style>