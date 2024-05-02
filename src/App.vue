<script lang="ts">
import Banner from './components/BannerCookinUp.vue'
import ConteudoPrincipal from './components/ConteudoPrincipal.vue'
import RodapePagina from './components/RodapePagina.vue'

export default {
  components: {
    Banner,
    ConteudoPrincipal,
    RodapePagina
  }
}
</script>

<template>
  <Banner />
  <ConteudoPrincipal />
  <RodapePagina />
</template>
