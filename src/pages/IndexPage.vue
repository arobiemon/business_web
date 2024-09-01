<template>
  <div class="q-pa-xl bg_gradian row">
    <div class="col-6">
      <div class="text-h2 text-bold">Pradictable Growth Starts here.</div>
      <div>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti optio
        debitis tenetur similique neque esse facere amet earum recusandae, ipsa
        voluptatibus repellendus. Perspiciatis rem dolorem quibusdam natus ea
        labore mollitia?
      </div>

      <q-btn
        label="Get Started"
        @click="onClick"
        class="q-mt-md"
        no-caps
        no-wrap
        unelevated
        :style="{
          background: 'linear-gradient(90deg, #1e3a8a, #3b82f6)',
          color: '#fff',
        }"
      />
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "IndexPage",
});
</script>

<style scoped>
.bg_gradian {
  background: rgb(164, 63, 251);
  background: radial-gradient(
    circle,
    rgba(164, 63, 251, 1) 0%,
    rgba(255, 255, 255, 0.8408613445378151) 34%
  );
}
</style>
