<script>
export default {
  data() {
    return {
      tab: '1'
    }
  }
}
</script>

<template>
  <h2>Conditional v-if on &lt;template&gt;</h2>

  <p>
    Por <i>v-if</i> ser uma diretiva, ela deve ser anexada a um único elemento.<br>
    Mas e se quisermos alternar mais de um elemento?<br>
    Neste caso podemos usar <i>v-if</i> em um elemento &lt;template&gt;, que serve como um embrulho invisível.<br>
    O resultado final renderizado não incluirá o elemento &lt;template&gt;.
  </p>

  <template v-if="tab === '1'">
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Veritatis aspernatur molestiae</p>
  </template>
  <template v-else-if="tab === '2'">
    <p>Optio obcaecati officia, soluta quas est.</p>
    <p>Magni non facilis hic, quaerat at optio impedit beatae minima.</p>
  </template>

  <!--
    Ignore this code snippet, you can learn about clicking on the (Form Input Bindings) subproject!
    https://vuejs.org/guide/essentials/forms.html#v-model-with-components
  -->
  <select v-model="tab">
    <option value="1">Aba 1</option>
    <option value="2">Aba 2</option>
  </select>

</template>