<template>
  <q-layout>
    <q-header style="background: #ffffff !important; color: black">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="favorite"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <div class="col-12 col-md-3">
          <q-toolbar-title class="text-bold">Cool Art Lab</q-toolbar-title>
        </div>

        <div class="col-12 col-md-3">Home</div>
        <div class="col-12 col-md-3">About</div>
        <div class="col-12 col-md-3">Contact</div>
      </q-toolbar>
    </q-header>

    <q-footer style="background: blue-6">
      <div class="fotterClass row">
        <div class="col-12 col-md-3">
          <div class="text-bold">INFO</div>
          <div>Formats</div>
          <div>Compression</div>
          <div>Pricing</div>
          <div>FAQ</div>
          <div>Status</div>
        </div>
        <div class="col-12 col-md-3">
          <div class="text-bold">RESOURCES</div>
          <div>Developer API</div>
          <div>Tools</div>
          <div>Blog</div>
        </div>
        <div class="col-12 col-md-3">
          <div class="text-bold">COMPANY</div>
          <div>About Us</div>
          <div>Sustainability</div>
          <div>Terms of Service</div>
          <div>Privacy</div>
        </div>
        <div class="col-12 col-md-3">
          <div class="row q-mb-sm">Subscribe to our email newsletter.</div>

          <q-form>
            <div class="row q-pb-lg">
              <div class="col-6">
                <q-input
                  class="row"
                  type="email"
                  dense
                  color="white"
                  label="Your email"
                  outlined
                  placeholder="email@gmail.com"
                  lazy-rules
                  :rules="[
                    (val) =>
                      (val && val.length > 0) || '*Please enter your email',
                  ]"
                />
              </div>
              <div class="col-6">
                <div class="q-ml-sm">
                  <q-btn
                    label="Subscribe"
                    no-caps
                    outline
                    type="submit"
                    color="white"
                  />
                </div>
              </div>
            </div>
          </q-form>
          <div class="row q-mb-sm">Follow Us</div>
          <div class="row q-mb-sm">
            <q-icon size="30px" name="facebook" />
            <q-icon size="30px" name="cake" />
            <q-icon size="30px" name="public" />
          </div>
        </div>
      </div>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

defineOptions({
  name: "MainLayout",
});

const isOutline = ref(false);
const linksList = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
<style lang="scss" scoped>
@media only screen and (max-width: 600px) {
  .fotterClass {
    margin: 5px;
  }
}
@media only screen and (min-width: 600px) {
  .fotterClass {
    margin: 15px;
  }
}
.ighyugyugbyhu {
  border-radius: 50%;
}
</style>
