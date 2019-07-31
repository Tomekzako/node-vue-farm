<template>
  <Details 
    :product="products[id]"/>
</template>

<script>
import Details from '@/components/productDetails'
export default {
  components: {
    Details
  },
  data() {
    return {
      id: 0
    }
  },
  computed: {
    products() {
      return this.$store.getters.getProducts
    }
  },
  mounted() {
   this.id = this.$nuxt._route.params.id 
  }
}
</script>

