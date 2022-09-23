<script>
export default {
  data() {
    return {
      number: 2,
      ok: true,
      message: 'Hello World!',
      id: 324
    }
  }
}
</script>

<template>

  <h1>Usando Expressões JavaScript</h1>

  <p>
    O Vue possui suporte a Expressões JavaScript no Text Interpolation e também no Attribute Bindings(v-bind):
    <br>
    {{ number + 1 }}
    <br>
    {{ ok ? 'YES' : 'NO' }}
    <br>
    {{ message.split('').reverse().join('') }}
    <br>
    <div :id="`list-${id}`"></div>
  </p>

  <p>
    Cada ligação pode conter apenas uma única expressão.<br>
    Uma expressão é um pedaço de código que pode resultar em um valor.<br>
    Uma verificação simples é se ele pode ser usado após <b>return</b>.<br>
    Portanto, o seguinte NÃO funcionará:
  </p>

  <textarea v-pre disabled style="width: 624px; height: 110px;">
    <!-- Isso é uma afirmação, não uma expressão: -->
    {{ var a = 1 }}

    <!-- O controle de fluxo também não funcionará, use expressões ternárias -->
    {{ if (ok) { return message } }}
  </textarea>

  <p>Tambem é possível chamar um método/função exposto ao componente dentro de uma expressão de ligação.</p>

  <textarea v-pre disabled style="width: 624px; height: 75px;">
    <span :title="toTitleDate(date)">
      {{ formatDate(date) }}
    </span>
  </textarea>
</template>