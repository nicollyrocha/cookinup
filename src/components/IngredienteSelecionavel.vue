<script lang="ts">
import TagIngrediente from './TagIngrediente.vue'

export default {
  components: {
    TagIngrediente
  },
  props: {
    ingrediente: { type: String, required: true }
  },
  data() {
    return {
      selecionado: false
    }
  },
  methods: {
    aoClicar() {
      this.selecionado = !this.selecionado
      if (this.selecionado) {
        this.$emit('adicionarIngrediente', this.ingrediente)
      } else {
        this.$emit('removerIngrediente', this.ingrediente)
      }
    }
  },
  emits: ['adicionarIngrediente', 'removerIngrediente']
}
</script>

<template>
  <button class="ingrediente" v-on="{ click: () => aoClicar() }" :aria-pressed="selecionado">
    <TagIngrediente :texto="ingrediente" :ativa="selecionado" />
  </button>
</template>

<style scoped>
.ingrediente {
  cursor: pointer;
}
</style>
