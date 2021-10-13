<template>
  <div
    data-src="/demo/design-bites/images/bottom-bg.svg"
    uk-img=""
    class="uk-background-norepeat uk-background-contain uk-background-bottom-left uk-section uk-section-large"
    uk-parallax="bgx: -120,-120;bgy: 420,120;easing: 0.5"
    style='background-image: url("https://demo.yootheme.com/demo/design-bites/images/bottom-bg.svg"); background-position: calc(-120px) calc(100% + 412.86px);'
  >
    <div class="uk-container uk-container-xlarge">
      <div
        id="fonts"
        class="tm-grid-expand uk-child-width-1-1 uk-margin-xlarge uk-grid uk-grid-stack"
        uk-grid=""
      >
        <div class="uk-width-1-1@m uk-first-column">
          <h2
            class="uk-h3 uk-heading-bullet uk-scrollspy-inview "
            uk-scrollspy-class=""
            style=""
          >
            <a
              class="el-link uk-link-reset"
              href="/joomla/themes/design-bites/resources/fonts"
              >Job Offers</a
            >
          </h2>
          <div class="uk-margin-medium">
            <div
              class="uk-child-width-1-1 uk-child-width-1-2@s uk-child-width-1-4@m uk-grid-match uk-grid"
              uk-grid=""
            >
              <div v-for="offer in offers" class="uk-first-column">
                <nuxt-link :to="`/offer/${offer.id}`">
                <a
                  class="el-item uk-card uk-card-default uk-card-hover uk-link-toggle uk-display-block uk-scrollspy-inview "
                  uk-scrollspy-class=""
                  style=""
                >
                  <div class="uk-card-media-top">
                    <img
                      class="el-image"
                      alt=""
                      data-width="610"
                      data-height="407"
                      sizes="(min-width: 610px) 610px"
                      :src="`https://helica-admin.herokuapp.com${offer.image.url}`"
                    />
                  </div>
                  <div class="uk-card-body uk-margin-remove-first-child">
                    <h3
                      class="el-title uk-h5 uk-margin-top uk-margin-remove-bottom"
                    >
                      {{ offer.title }}
                    </h3>
                    <div class="el-meta uk-text-meta uk-margin-small-top">
                      {{ offer.metaDescription }}
                    </div>
                  </div>
                </a>
                </nuxt-link>
              </div>
         
            </div>
          </div>

        </div>
        <!-- End of it -->
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "OffersFilter",
  props: ['offers']
};
</script>
