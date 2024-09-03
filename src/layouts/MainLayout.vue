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

        <q-toolbar-title class="text-bold">Cool Art Lab</q-toolbar-title>

        <div>welcome Brother</div>
      </q-toolbar>
    </q-header>

    <q-footer style="background: blue-6">
      <div class="row">
        <div class="col-2">
          INFO
          <div>Formats</div>
          <div>Compression</div>
          <div>Pricing</div>
          <div>FAQ</div>
          <div>Status</div>
        </div>
        <div class="col-2">
          RESOURCES
          <div>Developer API</div>
          <div>Tools</div>
          <div>Blog</div>
        </div>
        <div class="col-2">
          COMPANY
          <div>About Us</div>
          <div>Sustainability</div>
          <div>Terms of Service</div>
          <div>Privacy</div>
        </div>
        <div class="col-6">
          <div class="q-pa-md" style="max-width: 300px">
            <q-form>
              <q-input
                filled
                type="email"
                v-model="name"
                label="Your email *"
                hint="email@gmail.com"
                lazy-rules
                :rules="[
                  (val) => (val && val.length > 0) || 'Please enter your email',
                ]"
              />
              <div>
                <q-btn label="Suscribe" type="submit" color="white" />
              </div>
            </q-form>
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
