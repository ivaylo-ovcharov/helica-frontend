<template>
    <div>
        <OffersFilter :offerFilters="offerFilters" />
        <OffersList :offers="filteredOffers"/>
    </div>
</template>

<script>
import OffersFilter from "~/components/OffersFilter.vue"
import OffersList from "~/components/OffersList.vue"

export default {
  data() {
    return {
      filteredOffers: [],
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
      this.filteredOffers = this.offers
      this.offerFilters = await this.$axios.$get('https://helica-admin.herokuapp.com/categories')
    } catch (error) {
      this.error = error
    }
  },
  components: {
    OffersFilter,
    OffersList
  },
  watch: { 
     '$route.query.slug': {
        handler: function(search) {
          if (search) {
            this.filteredOffers = this.offers.filter((e) => e.category.Name == this.$route.query.slug)
          } else {
            this.filteredOffers= this.offers
          }
           
        },
        deep: true,
        immediate: true
      }
}
}
</script>
