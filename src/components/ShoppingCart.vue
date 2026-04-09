<template>
  <div>
    <h2>Carrinho da Empresa Q</h2>
    <p>Itens no carrinho: {{ totalItens }}</p>
    
    <button @click="adicionar">Adicionar Produto de Teste</button>
  </div>
</template>

<script>
export default {
  computed: {
    totalItens() {
      // Acede ao Getter que criou no Passo 2
      return this.$store.getters.cartItemCount;
    }
  },
  methods: {
    adicionar() {
      const produtoFake = { id: 1, nome: 'Produto XPTO' };
      // Dispara a Action que criou no Passo 2
      this.$store.dispatch('addToCart', produtoFake);
    }
  }
}
</script>