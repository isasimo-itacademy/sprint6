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

<style scoped>
.escena {
  background-color: rgb(225 236 249);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

li {
  border: 2px solid rgb(25, 24, 26);
  border-radius: 25px;
  list-style: none;
  padding: 10px;
  margin-bottom: 5px;
}

</style>