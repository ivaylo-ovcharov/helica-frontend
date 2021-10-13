<template>
  <div
    class="uk-section-muted uk-section uk-section-xlarge uk-padding-remove-bottom"
    tm-header-transparent="dark"
    uk-scrollspy="target: [uk-scrollspy-class]; cls: uk-animation-fade; delay: false;"
  >
    <div class="uk-container">
      <div
        class="tm-header-placeholder uk-margin-remove-adjacent"
        style="height: 0px;"
      ></div>
      <div
        class="tm-grid-expand uk-child-width-1-1 uk-grid-margin uk-grid uk-grid-stack"
        uk-grid=""
      >
        <div class="uk-grid-item-match uk-width-1-1@m uk-first-column">
          <div class="uk-panel uk-width-1-1">
            
            <div
              id="page#0-0-0-0"
              class="uk-position-absolute uk-width-1-1 uk-text-left"
              uk-parallax="y: 0,-9vh; easing: 0.5;"
              style="right: 33vw; top: -15vh; transform: translateY(0vh);"
            >
              <img
                class="el-image"
                alt=""
                target="!*"
                data-src="/demo/design-bites/images/resources-hero-left.svg"
                uk-img=""
                src="https://demo.yootheme.com/demo/design-bites/images/resources-hero-left.svg"
              />
            </div>

            <h1
              class="uk-heading-large uk-font-primary uk-position-relative uk-text-center uk-scrollspy-inview "
              style="z-index: 3;"
              uk-scrollspy-class=""
            >
              Find the best job positions for you
            </h1>
            <div
              class="uk-position-relative uk-margin-large uk-text-center"
              style="z-index: 3;"
            >
              <div
                class="uk-child-width-auto uk-flex-center uk-grid-small uk-grid-match uk-grid"
                uk-grid=""
              >
                <div v-for="filter in offerFilters" class="uk-first-column">
                  <nuxt-link :to="`/offers/?slug=${filter.Name}`">
                  <a
                    class="el-item uk-margin-auto uk-width-small uk-card uk-card-default uk-card-small uk-card-hover uk-card-body uk-margin-remove-first-child uk-link-toggle uk-display-block uk-scrollspy-inview "
                    uk-scrollspy-class=""
                    style=""
                  >
                    <div
                      class="el-title uk-h5 uk-margin-top uk-margin-remove-bottom"
                    >
                      {{ filter.Name }}
                    </div>
                  </a>
                  </nuxt-link>
                </div>
              </div>
            </div>
            <div
              id="page#0-0-0-3"
              class="uk-position-absolute uk-width-1-1 uk-text-right"
              uk-parallax="y: 4vh,-10vh; easing: 0.5;"
              style="right: -30vw; bottom: -30vh; transform: translateY(4vh);"
            >
              <img
                class="el-image"
                alt=""
                target="!*"
                data-src="/demo/design-bites/images/resources-hero-right.svg"
                uk-img=""
                src="demo/design-bites/images/resources-hero-right.svg"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  
</template>
<script>
export default {
  name: "OffersFilter",
  props: ['offerFilters'],
  data () {
    return {
      filterOptions: [
        {
          name: 'Cookers'
        },
        {
          name: 'Waitress'
        },
        {
          name: 'Hookers'
        },
        {
          name: 'Jogoloes'
        },
         {
          name: 'Stipperz'
        }
      ]
    }
  }
};
</script>
