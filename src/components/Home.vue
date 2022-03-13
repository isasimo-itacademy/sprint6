<script>
import EscenaComponent from './EscenaComponent.vue'

export default {
  name: 'HomeComponent',
  components: {
    EscenaComponent
  }
}
</script>

<template>
  <div class="home">
    <H2>Home</H2>
    <EscenaComponent />
  </div>
</template>

<style>
.home {
  background-color: yellow;
  font-weight: bold;
  padding: 10px;
}
</style>