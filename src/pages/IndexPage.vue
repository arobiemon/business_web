<template>
  <div>
    <div class="q-pa-xl bg_gradian">
      <div class="row">
        <div class="col-6">
          <div class="text-h2 text-bold">Predictable Growth Starts here.</div>
          <div>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti
            optio debitis tenetur similique neque esse facere amet earum
            recusandae, ipsa voluptatibus repellendus. Perspiciatis rem dolorem
            quibusdam natus ea labore mollitia?
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
      <div class="q-mt-md icons-container">
        <q-icon name="facebook" size="30px" color="black" />
        <q-icon name="facebook" size="30px" color="black" />
        <q-icon name="facebook" size="30px" color="black" />
        <q-icon name="facebook" size="30px" color="black" />
      </div>
    </div>
    <div>
      <div class="centered-text text-h4">
        Turn data into better business outcomes.
      </div>
      <div class="centered-lorem">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Obcaecati
        dignissimos rem qui modi ipsam laboriosam vel dolorem necessitatibus
        illo tempora, sed sit neque velit debitis molestias, numquam, dolores
        fugiat animi! Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Inventore similique corporis neque fugit sapiente aspernatur quam alias,
        pariatur recusandae nemo nostrum veritatis quo unde provident. Aut iure
        doloribus culpa quisquam?
      </div>
      <div class="q-pa-xl row centered-cols">
        <div class="col">
          <div class="text-bold text-h3">300%</div>
          <div>increase in new pipeline generated</div>
        </div>
        <q-separator vertical />
        <div class="col">
          <div class="text-bold text-h3">70%</div>
          <div>increase in from conversions</div>
        </div>
        <q-separator vertical />
        <div class="col">
          <div class="text-bold text-h3">60%</div>
          <div>Decrease in cost per lead</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "IndexPage",
});
</script>

<style scoped>
.wrapper {
  text-align: center;
}

.bg_gradian {
  background: rgb(63, 251, 227);
  background: radial-gradient(
    circle,
    rgba(63, 251, 227, 1) 0%,
    rgba(32, 230, 125, 1) 100%
  );
}

.icons-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 60px;
}

.centered-text {
  text-align: center;
  /* font-size: 20px; */
  font-weight: bold;
  margin-top: 20px;
}

.centered-lorem {
  text-align: center;
  margin-top: 10px;
  padding: 0 20px;
}
.centered-cols {
  display: flex;
  justify-content: center;
  text-align: center;
  color: rgba(44, 148, 204, 0.856);
}
.col {
  flex: 0 1 300px;
}
</style>
