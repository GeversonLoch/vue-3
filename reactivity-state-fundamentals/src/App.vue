<script>
import ReactiveState from './components/ReactiveState.vue'
import DeclaringMethods from './components/DeclaringMethods.vue'
import StatefulMethods from './components/StatefulMethods.vue'
import NextTick from './components/NextTick.vue'

export default {
  components: {
    ReactiveState,
    DeclaringMethods,
    StatefulMethods,
    NextTick
  }
}
</script>

<template>
  <h1>Reactivity State Fundamentals</h1>

  <ReactiveState/>
  <hr>
  <DeclaringMethods/>
  <hr>
  <StatefulMethods/>
  <hr>
  <NextTick/>

  <a href="https://vuejs.org/guide/essentials/reactivity-fundamentals.html" target="_blank">
    Vue 3 - Fundamentos de Reatividade
  </a>
</template>

<style>
/* Basic CSS for the page, ignore this! */
h1 { color: #42B883; }
h2,h3,h4 { color: #424242; }
p { color:#616161; }
</style>
