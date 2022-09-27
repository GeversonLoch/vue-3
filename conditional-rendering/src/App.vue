<script>
import VIf from './components/VIf.vue'
import VElse from './components/VElse.vue'
import VElseIf from './components/VElseIf.vue'
import VIfOnTemplate from './components/VIfOnTemplate.vue'
import VShow from './components/VShow.vue'

export default {
  components: {
    VIf,
    VElse,
    VElseIf,
    VIfOnTemplate,
    VShow
  }
}
</script>

<template>
  <h1>Conditional Rendering</h1>

  <VIf />
  <hr>
  <VElse/>
  <hr>
  <VElseIf/>
  <hr>
  <VIfOnTemplate/>
  <hr>
  <VShow/>

</template>

<style>
/* Basic CSS for the page, ignore this! */
h1 { color: #42B883; }
h2,h3,h4 { color: #424242; }
p { color:#616161; }
</style>
