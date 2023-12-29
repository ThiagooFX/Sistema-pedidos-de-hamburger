<template>
  <navbar />
  <make />
  <rodape />
</template>

<script>
import navbar from './components/navbar.vue'
import make from './components/make.vue'
import rodape from './components/rodape.vue'


export default {
  name: 'App',
  components: {
    navbar, make, rodape,
  }
}
</script>

<style>

  *{
    margin: 0;
    padding: 0;
  }
</style>
