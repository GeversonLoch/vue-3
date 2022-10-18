<script>
export default {
  data() {
    return {
      firstName: 'Geverson',
      lastName: 'Loch'
    }
  },
  computed: {
    fullName: { // Repare que desta vez é passado uma propriedade e não um metodo!
      get() { // Getter
        return `${this.firstName} ${this.lastName}`
      },
      set(newName) { // Setter
        [this.firstName, this.lastName] = newName.split(' ')
        // Nota: estamos usando a sintaxe de atribuição de desestruturação aqui.
      }
    }
  }
}
</script>

<template>
  <p>Meu nome é: {{ firstName }}</p>
  <p>Meu sobrenome é: {{ lastName }}</p>
  <p>Meu nome completo é: {{ fullName }}</p>
  <input type="text" v-model="fullName">
  <button @click="fullName = 'John Doe'">Alterar nome: John Doe</button>
</template>