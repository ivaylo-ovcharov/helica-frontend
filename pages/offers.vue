<template>
    <div>
        <OffersFilter :offerFilters="offerFilters" />
        <OffersList :offers="offers"/>
    </div>
</template>

<script>
import OffersFilter from "~/components/OffersFilter.vue"
import OffersList from "~/components/OffersList.vue"

export default {
  data() {
    return {
      offers: [],
      offerFilters: [],
      storeUrl: process.env.storeUrl,
      error: null
    }
  },
  async mounted() {
    try {
      // const response = await $http.$get('https://helica-admin.herokuapp.com/offers') 
      this.offers = await this.$axios.$get('https://helica-admin.herokuapp.com/offers')
      this.offerFilters = await this.$axios.$get('https://helica-admin.herokuapp.com/categories')
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
