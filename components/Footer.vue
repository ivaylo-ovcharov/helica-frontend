<template>
  <div>
    <div
      class="
        uk-section-default uk-section uk-section-large uk-padding-remove-bottom
      "
    >
      <div class="uk-container uk-container-xlarge">
        <div
          class="tm-grid-expand uk-grid-row-large uk-grid-margin-large uk-grid"
          uk-grid=""
        >
          <div class="uk-width-1-2@m uk-first-column">
            <div class="uk-h3 uk-text-left@m uk-text-center">
              
              Tourism jobs that<br class="uk-visible@s" />suits you best.
            </div>
          </div>

          <div
            class="
              uk-width-1-3 uk-width-expand@m uk-grid-margin uk-first-column
            "
          >
            <h3 class="uk-h5 uk-text-left@m uk-text-center">Company</h3>
            <ul class="uk-list uk-text-left@m uk-text-center">
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >About Us</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Success Stories</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Blog</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Services</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Careers</a
                  >
                </div>
              </li>
            </ul>
          </div>

          <div class="uk-width-1-3 uk-width-expand@m uk-grid-margin">
            <h3 class="uk-h5 uk-text-left@m uk-text-center">Resources</h3>
            <ul class="uk-list uk-text-left@m uk-text-center">
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Studio</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Culture</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Awards</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Archieve</a
                  >
                </div>
              </li>
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Contact</a
                  >
                </div>
              </li>
            </ul>
          </div>

          <div class="uk-width-1-3 uk-width-expand@m uk-grid-margin">
            <h3 class="uk-h5 uk-text-left@m uk-text-center">Social</h3>
            <ul class="uk-list uk-text-left@m uk-text-center">
              <li class="el-item">
                <div class="el-content uk-panel">
                  <a
                    href="https://www.facebook.com/helica.aeonlix"
                    class="el-link uk-link-muted uk-margin-remove-last-child"
                    >Facebook</a
                  >
                </div>
              </li>
            </ul>
          </div>
        </div>
        <div
          class="
            tm-grid-expand
            uk-child-width-1-1 uk-margin-xlarge uk-grid uk-grid-stack
          "
          uk-grid=""
        >
          <div class="uk-width-1-1@m uk-first-column">
            <hr />
          </div>
        </div>
      </div>
    </div>
    <div class="uk-section-default uk-section uk-section-small">
      <div class="uk-container uk-container-xlarge">
        <div
          class="
            tm-grid-expand
            uk-grid-row-small uk-grid-margin-small uk-grid uk-grid-stack
          "
          uk-grid=""
        >
          <div class="uk-width-auto@m uk-first-column">
            <div class="uk-margin-large uk-text-left@m uk-text-center">
              <a class="el-link" href="/joomla/themes/design-bites/index.php"
                ><img
                  class="el-image"
                  alt=""
                  uk-img=""
                  src="~/assets/Helica.svg"
                  width="80"
              /></a>
            </div>
          </div>

          <div
            class="
              uk-grid-item-match
              uk-flex-bottom
              uk-width-expand@m
              uk-grid-margin
              uk-first-column
            "
          >
            <div class="uk-panel uk-width-1-1">
              <div
                class="
                  uk-panel uk-text-meta uk-margin uk-text-right@m uk-text-center
                "
              >
                ©
                <script>
                  document.currentScript.insertAdjacentHTML(
                    "afterend",
                    '<time datetime="' +
                      new Date().toJSON() +
                      '">' +
                      new Intl.DateTimeFormat(document.documentElement.lang, {
                        year: "numeric",
                      }).format() +
                      "</time>"
                  );
                </script>
                <time datetime="2021-10-13T07:37:03.268Z">2021</time> Design
                Bites. All rights reserved.<br class="uk-hidden@s" />
                Powered by <a href="https://yootheme.com/">Entropy Active</a>.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Twitter from "~/components/icons/twitter.vue";
import Github from "~/components/icons/github.vue";
import Facebook from "~/components/icons/facebook.vue";

export default {
  components: {
    Twitter,
    Github,
    Facebook,
  },
};
</script>

<style>
.emoji {
  font-size: 30px;
}
</style>
