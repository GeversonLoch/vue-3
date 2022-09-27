<script>
export default {
  data() {
    return {
      data: true
    }
  }
}
</script>
  
<template>
  <h2>Conditional v-show</h2>

  <p>
    Outra opção para exibir condicionalmente um elemento é a diretiva <i>v-show</i>.<br>
    O uso é basicamente o mesmo:
  </p>

  <p v-show="data">Hello!</p>

  <p>
    A diferença é que um elemento com <i>v-show</i> sempre será renderizado e permanecerá no DOM;<br>
    <i>v-show</i> apenas alterna propriedade a display CSS do elemento.<br>
    <i>v-show</i> não suporta o elemento &lt;template&gt;, nem funciona com <i>v-else</i>.
  </p>

  <h3>v-if vs v-show</h3>

  <p>
    A renderização condicional <i>v-if</i> é "real" porque garante que os ouvintes de eventos <br>
    e os componentes filhos dentro do bloco condicional sejam destruídos <br>
    e recriados adequadamente durante as alternâncias.
  </p>

  <p>
    <i>v-if</i> também é <i>lazy</i>: Se a condição for falsa na renderização inicial, não fará nada - o bloco <br>
    condicional não será renderizado até que a condição se torne verdadeira pela primeira vez.
  </p>

  <p>
    Em comparação, <i>v-show</i> é muito mais simples - o elemento é sempre renderizado independentemente<br>
    da condição inicial, com alternância baseada em CSS.
  </p>

  <p>
    De um modo geral, <i>v-if</i> tem custos de alternância mais altos, <br>
    enquanto <i>v-show</i> tem custos de renderização iniciais mais altos.
  </p>

  <p>
    <b>
      Portanto, prefira <i>v-show</i> se precisar alternar algo com muita frequência<br>
      e prefira <i>v-if</i> se for improvável que a condição mude em tempo de execução.
    </b>
  </p>

</template>