<script>
import TextInterpolation from './components/TextInterpolation.vue'
import RawHTML from './components/RawHTML.vue'
import AttributeBindings from './components/AttributeBindings.vue'
import JavaScriptExpressions from './components/JavaScriptExpressions.vue'

export default {
  components: {
    TextInterpolation,
    RawHTML,
    AttributeBindings,
    JavaScriptExpressions
  }
}
</script>

<template>

  <h1>Template Syntax</h1>
  <p>
    O Vue usa uma sintaxe de modelo baseada em HTML que permite vincular <br>
    declarativamente o DOM renderizado aos dados da instância do componente subjacente.
  </p>

  <hr>

  <TextInterpolation />
  <hr>
  <RawHTML />
  <hr>
  <AttributeBindings />
  <hr>
  <JavaScriptExpressions />

</template>