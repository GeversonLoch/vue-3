<script>
import ComputedProperties from './components/ComputedProperties.vue'
import ComputedPropertiesVsMethods from './components/ComputedPropertiesVsMethods.vue'
import WritableComputed from './components/WritableComputed.vue'

export default {
  components: {
    ComputedProperties,
    ComputedPropertiesVsMethods,
    WritableComputed
  }
}
</script>

<template>
  <h1>Computed Properties</h1>

  <a href="https://vuejs.org/guide/essentials/computed.html" target="_blank">
    Vue 3 - Computed Properties
  </a>

  <ComputedProperties />
  <hr>
  <ComputedPropertiesVsMethods />
  <hr>
  <WritableComputed />
</template>

<style>
/* Basic CSS for the page, ignore this! */
h1 { color: #42B883; }
h2,h3,h4 { color: #424242; }
p { color:#616161; }
</style>
