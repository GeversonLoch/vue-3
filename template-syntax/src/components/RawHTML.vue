<script>
export default {
  data() {
    return {
      rawHtml: '<i>Agora podemos utilizar <b style="color: blue;">HTML</b> dentro da string</i>!'
    }
  }
}
</script>
  
<template>

  <h2>Raw HTML (v-html="htmlString")</h2>

  <p>
    O Text Interpolation interpreta os dados como texto simples, não HTML.<br>
    Para gerar HTML real, você precisará usar a diretiva <b>v-html</b>
  </p>

  <p>Usando Text Interpolation: {{ rawHtml }}</p>

  <p>Usando diretiva <code>v-html="rawHtml"</code>: <span v-html="rawHtml"></span></p>

  <a href="https://vuejs.org/guide/essentials/template-syntax.html#raw-html" target="_blank">Vue 3 - Raw HTML</a>

</template>