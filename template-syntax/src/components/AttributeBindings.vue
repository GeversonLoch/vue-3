<script>
export default {
  data() {
    return {
      cssString: 'color: #42B883; text-decoration-line: underline; text-decoration-style: dashed;',
      cssClass: 'css-class',
      isButtonDisabled: true,
      objectOfAttrs: {
        class: 'css-class',
        href: 'https://vuejs.org/guide/essentials/template-syntax.html#attribute-bindings',
        target: '_blank'
      },
      attributeName: 'href',
      url: 'https://vuejs.org/guide/essentials/template-syntax.html#dynamic-arguments'
    }
  }
}
</script>

<template>
  <h2>Attribute Bindings(v-bind)</h2>

  <p>
    A diretiva <b>v-bind</b> instrui o Vue a manter o <b>atributo</b> do elemento(tag)
    em sincronia com a propriedade informada no <code>data() { return  { property: true } }</code>.<br>
    <b>Se o valor vinculado for null ou undefined, o atributo será removido do elemento renderizado.</b>
  </p>

  <p v-bind:style="cssString">Veja meu style adquirido pelo <code>v-bind:style="cssString"</code></p>

  <h4>Forma abreviada</h4>

  <p>Por <b>v-bind</b> ser tão comumente usado, ele possui uma sintaxe abreviada dedicada
    <code>:href="link"</code>
  </p>

  <p :class="cssClass">Veja meu style adquirido pelo <code>:class="cssClass"</code></p>

  <h4>Atributos booleanos</h4>

  <p>
    Atributos booleanos são atributos que podem indicar valores verdadeiro/falso por sua presença em um elemento.<br>
    Por exemplo, <b>disabled</b> é um dos atributos booleanos mais usados.
  </p>

  <p>
    O disabledatributo será incluído se isButtonDisabledtiver um valor de verdade.<br>
    Também será incluído se o valor for uma string vazia, mantendo a consistência com
    <code>&lt;button disabled=""&gt;</code>.<br>
  </p>

  <button :disabled="isButtonDisabled">v-bind:disabled="isButtonDisabled"</button>
  <button :disabled="isButtonDisabled">:disabled="isButtonDisabled"</button>
  <button :disabled="''">:disabled="''"</button>


  <h4>Dynamically Binding Multiple Attributes</h4>

  <p>
    Você também poderá vincular múltiplos atributos simultaneamente,<br>
    se você tiver um objeto JavaScript representando vários atributos parecidos com este:
    <tag>v-bind="objectOfAttrs"</tag>
  </p>

  <p>
    <code>
      data() {
        return {
          objectOfAttrs: {
            class: 'css-class',
            href: 'https://vuejs.org/guide/essentials/template-syntax.html#attribute-bindings',
            target: '_blank'
          }
        }
      }
    </code>
  </p>

  <a v-bind="objectOfAttrs">Vue 3 - Dynamically Binding Multiple Attributes</a>

  <h4>Dynamic Arguments</h4>

  <p>Também é possível usar uma expressão JavaScript em um argumento de diretiva envolvendo-o com colchetes:</p>

  <!-- Observe que há algumas restrições para a expressão de argumento, 
  conforme explicado nas seções "Restrições de valor de argumento dinâmico" 
  e "Restrições de sintaxe de argumento dinâmico" abaixo. -->
  <a v-bind:[attributeName]="url" target="_blank">Dynamic Arguments</a>
  <br>
  <!-- Abreviação -->
  <a :[attributeName]="url" target="_blank">Abreviação dos Dynamic Arguments</a>

  <p>
    Aqui <b>attributeName</b> será avaliado dinamicamente como uma expressão JavaScript,<br>
    e seu valor avaliado será usado como valor final para o argumento.<br>
    Por exemplo, se a instância do seu componente tiver uma propriedade de dados,<br>
    <b>attributeName</b>, cujo valor é "href", essa associação será equivalente a v-bind:href.
  </p>

  <h4>Restrições do Dynamic Arguments</h4>

  <p>
    Expressões de argumentos dinâmicos têm algumas restrições de sintaxe porque certos caracteres,<br>
    como espaços e aspas, são inválidos dentro de nomes de atributos HTML.<br>
    Por exemplo, o seguinte é inválido:
  </p>

  <textarea v-pre disabled style="width: 624px; height: 60px;">
    Isso acionará um aviso do compilador!

    <a :[&apos;foo&apos; + bar]=&quot;value&quot;>...</a>
  </textarea>

</template>

<style>
.css-class {
  color: crimson;
  text-decoration-line: underline;
  text-decoration-style: dotted;
}
</style>