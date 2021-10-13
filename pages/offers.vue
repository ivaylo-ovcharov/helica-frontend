<template>
    <div>
        <OffersFilter />
        <OffersList />
    </div>
</template>

<script>
import OffersFilter from "~/components/OffersFilter.vue"
import OffersList from "~/components/OffersList.vue"

export default {
  data() {
    return {
      products: [],
      storeUrl: process.env.storeUrl,
      error: null
    }
  },
  async mounted() {
    try {
      this.products = await this.$strapi.$products.find()
    } catch (error) {
      this.error = error
    }
  },
  components: {
    OffersFilter,
    OffersList
  }
}
</script>
