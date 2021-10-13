<template>
  <div
    v-if="offer"
    class="uk-section-muted uk-section uk-section-large"
    tm-header-transparent="dark"
  >
    <div class="uk-container">
      <div
        class="tm-header-placeholder uk-margin-remove-adjacent"
        style="height: 100px;"
      ></div>
      <div
        class="tm-grid-expand uk-grid-column-large uk-grid-margin uk-grid"
        uk-grid=""
      >
        <div class="uk-width-1-3@m uk-first-column">
          <div>
            <ul class="uk-breadcrumb uk-margin-remove-bottom">
              <li>
                <nuxt-link to="/offers">
                  <a>🔙 Back to offers</a>
                </nuxt-link>
              </li>
            </ul>
          </div>

          <h1 class="uk-heading-small">{{ offer.title }} </h1>
          <div
            uk-slideshow="ratio: 3:2;"
            class="uk-hidden@m uk-margin uk-slideshow"
          >
            <div class="uk-position-relative">
              <ul class="uk-slideshow-items">
                <li v-for="img in offer.gallery" class="el-item" tabindex="-1">
                  <img
                    class="el-image uk-cover"
                    alt=""
                    uk-img="target: !.uk-slideshow-items"
                    data-sizes="(max-aspect-ratio: 900/600) 150vh"
                    data-width="900"
                    data-height="600"
                    :src='`${img.url}`'
                  />
                </li>
              </ul>
            </div>

            <ul
              class="el-nav uk-thumbnav uk-flex-left uk-margin-top"
              uk-margin=""
            >
              <li v-for="img in offer.gallery" uk-slideshow-item="0" class="uk-active">
                <a href="#"
                  ><img
                    alt=""
                    data-sizes="(min-width: 100px) 100px"
                    data-width="100"
                    data-height="75"
                    :src='`${img.url}`'
                /></a>
              </li>
            </ul>
          </div>
          <div class="uk-panel uk-margin-medium">
            {{ offer.description }}
          </div>
          <ul class="uk-list uk-margin-large uk-margin-remove-bottom">
            <li v-for="meta in metas" class="el-item">
              <div
                class="uk-child-width-expand uk-grid-column-medium uk-grid-row-small uk-grid"
                uk-grid=""
              >
                <div class="uk-width-small uk-text-break uk-first-column">
                  <div class="el-title uk-margin-remove uk-font-primary">
                    {{ meta.title }}
                  </div>
                </div>
                <div>
                  <div class="el-content uk-panel">
                    <a
                      class="uk-link-reset uk-margin-remove-last-child"
                      href="/joomla/themes/design-bites/resources/vectors/29-illustrations"
                      > {{ offer[meta.val] }}</a
                    >
                  </div>
                </div>
              </div>
            </li>
          </ul>
          <hr class="uk-margin-medium" />
          <div class="uk-panel uk-margin-remove-first-child uk-margin">
            <div
              class="uk-child-width-expand uk-grid-column-medium uk-flex-middle uk-grid"
              uk-grid=""
            >
              <div class="uk-width-auto uk-first-column">
                <img
                  class="el-image uk-border-circle"
                  alt=""
                  style="width: 80px; height: 80px"
                  data-sizes="(min-width: 80px) 80px"
                  data-width="80"
                  data-height="80"
                  sizes="(min-width: 80px) 80px"
                  src="https://scontent.fsof1-2.fna.fbcdn.net/v/t1.6435-9/56793246_119077965939617_5155880983538434048_n.jpg?_nc_cat=109&ccb=1-5&_nc_sid=174925&_nc_ohc=HzPmyQEe3jMAX8fJG01&_nc_ht=scontent.fsof1-2.fna&oh=bdd63a7846f1d66730188242b5f8dc91&oe=618A62F6"
                />
              </div>
              <div class="uk-margin-remove-first-child">
                <div
                  class="el-title uk-h5 uk-font-primary uk-margin-top uk-margin-remove-bottom"
                >
                  Human Recourses
                </div>

                <div class="el-content uk-panel">Svetla Milcheva</div>
              </div>
            </div>
          </div>
          <div class="uk-margin-large">
            <a
              class="el-content uk-width-1-1 uk-button uk-button-primary uk-button-large"
              target="_blank"
              :href="offer.applylinlk"
            >
              Apply
            </a>
          </div>
        </div>

        <div class="uk-width-2-3@m uk-visible@m">
          <div class="uk-visible@m uk-margin">
            <div
              class="uk-child-width-1-1 uk-grid-match uk-grid uk-grid-stack"
              uk-grid=""
            >
              <div v-for="img in offer.gallery" class="uk-first-column">
                <div class="el-item uk-panel uk-margin-remove-first-child">
                  <img
                    class="el-image uk-border-rounded"
                    alt=""
                    data-sizes="(min-width: 1600px) 1600px"
                    data-width="1600"
                    data-height="1067"
                    sizes="(min-width: 1600px) 1600px"
                    :src='`${img.url}`'
                  />
                </div>
              </div>

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
  data() {
    return {
      offer: null,
      metas: [
        {
          title: 'Country',
          val: 'metaCountry'
        },
        {
          title: 'Region',
          val: 'metaRegion'
        },
        {
          title: 'Position',
          val: 'metaJobPosition'
        },
        {
          title: 'Salary',
          val: 'metaSalary'
        },
        {
          title: 'Working Hours',
          val: 'metaWorkingHours'
        },
        {
          title: 'Working Days',
          val: 'metaWorkingDays'
        },
        {
          title: 'Occupation',
          val: 'metaOccupation'
        }
      ]
    }
  },
   async mounted() {
    try {
      // const response = await $http.$get('https://helica-admin.herokuapp.com/offers') 
      this.offer = await this.$axios.$get(`https://ivaylo-portfolio.herokuapp.com/a-offers/${this.$route.params.id}`)
    } catch (error) {
      this.error = error
    }
  },
};
</script>
