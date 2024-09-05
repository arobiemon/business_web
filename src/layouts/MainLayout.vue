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
          @click="drawerLeft = !drawerLeft"
        />
        <q-toolbar-title class="text-bold">Cool Art Lab</q-toolbar-title>
        <!--for app bar added-->
        <q-btn label="Home" @click="onClick" to="/" />
        <q-btn class="q-mx-md" label="About" to="/about" />
        <q-btn label="Contact Us" @click="onClick" to="/contact" />
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

    <q-drawer
      side="right"
      v-model="drawerLeft"
      show-if-above
      bordered
      :width="200"
      :breakpoint="500"
    >
      <q-scroll-area class="fit">
        <div class="q-pa-sm">
          <div v-for="n in 50" :key="n">Drawer {{ n }} / 50</div>
        </div>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      drawerLeft: ref(false),
    };
  },
};
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
