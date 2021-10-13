<template>
  <div>
    <div
      class="
        uk-section-muted uk-section uk-section-xlarge uk-padding-remove-bottom
      "
      tm-header-transparent="dark"
      uk-scrollspy="target: [uk-scrollspy-class]; cls: uk-animation-fade; delay: false;"
    >
      <div class="uk-container uk-container-xlarge">
        <div
          class="tm-header-placeholder uk-margin-remove-adjacent"
          style="height: 0px"
        ></div>
        <div
          class="
            tm-grid-expand
            uk-child-width-1-1 uk-grid-margin uk-grid uk-grid-stack
          "
          uk-grid=""
        >
          <div class="uk-grid-item-match uk-width-1-1@m uk-first-column">
            <div class="uk-panel uk-width-1-1">
              <div
                id="page#0-0-0-0"
                class="uk-position-absolute uk-width-1-1 uk-text-left"
                uk-parallax="y: 0,-9vh; easing: 0.5;"
                style="right: 30vw; top: -16vh; transform: translateY(0vh)"
              >
                <img
                  class="el-image"
                  alt=""
                  target="!*"
                  data-src="https://demo.yootheme.com/demo/design-bites/images/home-hero-left.svg"
                  uk-img=""
                  src="https://demo.yootheme.com/demo/design-bites/images/home-hero-left.svg"
                />
              </div>

              <h1
                class="
                  uk-heading-xlarge
                  uk-font-primary
                  uk-position-relative
                  uk-text-center
                  uk-scrollspy-inview
                "
                style="z-index: 3"
                uk-scrollspy-class=""
              >
                Awesome Design <br />Resources
              </h1>
              <div
                class="
                  uk-panel
                  uk-text-large
                  uk-position-relative
                  uk-margin-medium
                  uk-text-center
                  uk-scrollspy-inview
                "
                style="z-index: 3"
                uk-scrollspy-class=""
              >
                Explore Our Premium Design Assets to Reinforce Your Creative
                Flow
              </div>
              <div
                id="page#0-0-0-3"
                class="uk-position-absolute uk-width-1-1 uk-text-right"
                uk-parallax="y: 4vh,-10vh; easing: 0.5;"
                style="right: -20vw; bottom: -24vh; transform: translateY(4vh)"
              >
                <img
                  class="el-image"
                  alt=""
                  target="!*"
                  data-src="/demo/design-bites/images/home-hero-right.svg"
                  uk-img=""
                  src="https://demo.yootheme.com/demo/design-bites/images/home-hero-right.svg"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <HomeOffers />
  </div>
</template>

<script>
import Products from "~/components/Products.vue";
import HomeOffers from "~/components/HomeOffers.vue";

export default {
  data() {
    return {
      products: [],
      storeUrl: process.env.storeUrl,
      error: null,
    };
  },
  async mounted() {
    try {
      this.products = await this.$strapi.$products.find();
    } catch (error) {
      this.error = error;
    }
  },
  components: {
    Products,
    HomeOffers
  },
};
</script>
