<script>
import { nextTick } from 'vue'

export default {
  data() {
    return {
      text: 'No entanto, deve-se observar que as atualizações do DOM... ',
      count: 0
    }
  },
  methods: {
    increment() {

      debugger;
      this.text += 'não são aplicadas de forma sincrona com a reatividade.'
      console.info('Text is Updated!');

      nextTick(() => {
        debugger;
        console.info('Repare que arecem agora o DOM foi atualizado!');
      })

      debugger;
      this.count++
      console.info('Count is Updated!');

    }
  }
}
</script>

<template>
  <h2>Tempo de atualização do DOM e nextTick()</h2>

  <p>
    Quando você altera o estado reativo, o DOM é atualizado automaticamente.<br>
    <i style="color: red;">{{ text }}</i><br>
    Em vez disso, o Vue os armazena em buffer até o "próximo tick" no ciclo de atualização<br>
    para garantir que cada componente precise atualizar apenas uma vez,<br>
    não importa quantas alterações de estado você tenha feito.
  </p>

  <button @click="increment">NextTick: {{ count }}</button>

  <p>Para aguardar a conclusão da atualização do DOM após uma mudança de estado, você pode usar a API global nextTick()</p>

</template>