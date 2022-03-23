<template>
    <button @click="$emit('mostraAnterior')">Anterior</button>
    <button @click="$emit('mostraSeguent')">Següent</button>
</template>

<script>
export default {
  name: 'BotonsComponent',
  props: {
    currentSentence: Number
  }
}
</script>

<style>
    button {
        width: 40%;
        padding: 15px;
        background-color: white;
        border: 2px solid rgb(25, 24, 26);
        border-radius: 25px;
        margin: 20px;
        cursor: pointer;
    }
</style>