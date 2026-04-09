<template>
  <div id="app">
    <ShoppingCart />
  </div>
</template>

<script>
// Importando o componente que você criou
import ShoppingCart from './components/ShoppingCart.vue'

export default {
  name: 'App',
  components: {
    ShoppingCart // Registrando ele aqui
  }
}
</script>
