<template>
  <div class="container">
    <h1>🌽 Node Farm 🥦</h1>
    <div class="cards-container">
      <Product 
        v-for="product in products"
        :key="product.id"
        :product="product"
        @click.native="openProduct(product.id)"/>
    </div>
  </div>
</template>

<script>
import Product from '~/components/productOverview.vue'

export default {
  components: {
    Product
  },
  computed: {
    products() {
      return this.$store.getters.getProducts
    }
  },
  methods: {
    openProduct(id) {
      this.$router.push(`/product/${id}`);
    }
  }
}
</script>

    <style>
.container {
  width: 95rem;
  margin: 0 auto;
}

.cards-container {
  margin-top: 8rem;
}
</style>
