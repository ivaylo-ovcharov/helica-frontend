<template>
  <div>
    <div class="tm-header-mobile uk-hidden@m">
      <div
        uk-sticky=""
        show-on-up=""
        animation="uk-animation-slide-top"
        cls-active="uk-navbar-sticky"
        sel-target=".uk-navbar-container"
        class="uk-sticky"
        style=""
      >
        <div class="uk-navbar-container">
          <nav uk-navbar="container: .tm-header-mobile" class="uk-navbar">
            <div class="uk-navbar-center">
              <nuxt-link to="/offers">
              <a
                class="uk-navbar-item uk-logo"
              >
                <img
                  alt="Design Bites"
                  src="https://demo.yootheme.com/demo/design-bites/images/logo-mobile.svg"
              /></a>
              </nuxt-link>
            </div>

            <div class="uk-navbar-right">
              <a
                class="uk-navbar-toggle"
                href="#tm-mobile"
                uk-toggle=""
                aria-expanded="false"
              >
                <div
                  uk-navbar-toggle-icon=""
                  class="uk-icon uk-navbar-toggle-icon"
                >
                  <svg
                    width="20"
                    height="20"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <rect y="9" width="20" height="2"></rect>
                    <rect y="3" width="20" height="2"></rect>
                    <rect y="15" width="20" height="2"></rect>
                  </svg>
                </div>
              </a>
            </div>
          </nav>
        </div>
      </div>
      <div
        class="uk-sticky-placeholder"
        style="height: 100px; margin: 0px"
        hidden=""
      ></div>

      <div
        id="tm-mobile"
        uk-offcanvas=""
        mode="push"
        overlay=""
        flip=""
        class="uk-offcanvas"
        style=""
        tabindex="0"
      >
        <div class="uk-offcanvas-bar uk-text-center uk-flex">
          <button
            class="uk-offcanvas-close uk-icon uk-close"
            type="button"
            uk-close=""
          >
            <svg
              width="14"
              height="14"
              viewBox="0 0 14 14"
              xmlns="http://www.w3.org/2000/svg"
            >
              <line
                fill="none"
                stroke="#000"
                stroke-width="1.1"
                x1="1"
                y1="1"
                x2="13"
                y2="13"
              ></line>
              <line
                fill="none"
                stroke="#000"
                stroke-width="1.1"
                x1="13"
                y1="1"
                x2="1"
                y2="13"
              ></line>
            </svg>
          </button>

          <div class="uk-margin-auto-vertical uk-width-1-1">
            <div class="uk-child-width-1-1 uk-grid uk-grid-stack" uk-grid="">
              <div class="uk-first-column">
                <div class="uk-panel" id="module-menu-mobile">
                  <ul class="uk-nav uk-nav-primary uk-nav-center">
                    <li class="item-108 uk-parent">
                      <nuxt-link to="/offers">
                      <a>
                        Offers</a
                      >
                      </nuxt-link>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="uk-grid-margin uk-first-column">
                <div class="uk-panel" id="module-91">
                  <div class="uk-margin-remove-last-child custom">
                    <nuxt-link to="/about">
                    <a
                      class="uk-button uk-button-secondary"
                      >About</a
                    >
                    </nuxt-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="tm-header uk-visible@m tm-header-overlay" uk-header="">
      <div
        uk-sticky=""
        media="@m"
        show-on-up=""
        animation="uk-animation-slide-top"
        cls-active="uk-navbar-sticky"
        sel-target=".uk-navbar-container"
        class="uk-sticky"
        style=""
      >
        <div class="uk-navbar-container uk-navbar-transparent uk-dark">
          <div class="uk-container uk-container-expand">
            <nav
              class="uk-navbar"
            >
              <div class="uk-navbar-left">
                <nuxt-link to="/">
                <a
                  class="uk-navbar-item uk-logo"
                >
                  <img
                    alt="Design Bites"
                    src="https://demo.yootheme.com/demo/design-bites/images/logo.svg" /><img
                    class="uk-logo-inverse"
                    alt="Design Bites"
y                /></a>
                </nuxt-link>
              </div>

              <div class="uk-navbar-right">
                <ul class="uk-navbar-nav">
                  <li class="item-108 uk-parent">
                    <nuxt-link to="/offers">
                    <a
                      aria-expanded="false"
                    >
                      Offers</a
                    >
                    </nuxt-link>
                  </li>
                </ul>

                <div class="uk-navbar-item" id="module-90">
                  <div class="uk-margin-remove-last-child custom">
                    <nuxt-link to="/about">
                    <a
                      class="uk-button uk-button-primary"
                      >About</a
                    >
                     </nuxt-link>
                  </div>
                </div>
              </div>
            </nav>
          </div>
        </div>

        <div
          class="uk-navbar-dropdown uk-navbar-dropdown-bottom-left"
          style="left: 1068.08px; top: 90px"
        >
          <div
            class="
              uk-navbar-dropdown-grid uk-child-width-1-1 uk-grid uk-grid-stack
            "
            uk-grid=""
          >
            <div class="uk-first-column">
              <ul class="uk-nav uk-navbar-dropdown-nav">
                <li class="item-124">
                  <a href="/joomla/themes/design-bites/resources/fonts">
                    Fonts</a
                  >
                </li>
                <li class="item-121">
                  <a href="/joomla/themes/design-bites/resources/brushes">
                    Brushes</a
                  >
                </li>
                <li class="item-119">
                  <a href="/joomla/themes/design-bites/resources/vectors">
                    Vectors</a
                  >
                </li>
                <li class="item-118">
                  <a href="/joomla/themes/design-bites/resources/graphics">
                    Graphics</a
                  >
                </li>
                <li class="item-109">
                  <a href="/joomla/themes/design-bites/resources/mockups">
                    Mockups</a
                  >
                </li>
                <li class="item-120">
                  <a href="/joomla/themes/design-bites/resources/ui-kits">
                    UI Kits</a
                  >
                </li>
                <li class="item-138">
                  <a href="/joomla/themes/design-bites/resources/view-all">
                    View All</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div
        class="uk-sticky-placeholder"
        style="height: 100px; margin: 0px"
        hidden=""
      ></div>
    </div>
  </div>
</template>

<script>
import Cart from "./icons/cart.vue";

export default {
  components: {
    Cart,
  },
};
</script>

<style>
.emoji {
  font-size: 30px;
}
</style>
