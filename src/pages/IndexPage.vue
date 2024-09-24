<template>
  <div>
    <div class="q-pa-xl bg_gradian col-12 col-md-6">
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
      <div class="q-mt-md row flex-center icons-container">
        <q-icon name="facebook" size="30px" color="black" />
        <q-icon name="facebook" size="30px" color="black" />
        <q-icon name="facebook" size="30px" color="black" />
        <q-icon name="facebook" size="30px" color="black" />
      </div>
    </div>
    <div class="col-12 col-md-6 q-pa-md">
      <div class="text-h4 row flex-center q-pt-lg text-bold">
        Turn data into better business outcomes.
      </div>
      <div class="row flex-center centered-lorem">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur,
        animi. Hic consequuntur et soluta, ea nisi ipsam saepe, nihil obcaecati,
        sunt corporis quas accusantium harum eos sit fuga vero vitae. Lorem
        ipsum dolor sit amet, consectetur adipisicing elit. Magni deserunt eaque
        tenetur et eum dolorum! Assumenda numquam neque ratione soluta incidunt
        ducimus omnis unde porro.
      </div>
      <div class="q-pa-xl centered-cols row flex-center">
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
      <div class="row flex-center">
        <q-btn
          label="Explore the platfrom"
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
    <div class="q-pa-xl row">
      <div class="col-12 col-md-6">
        <q-img
          src="~assets/Mr. Mike.png"
          :ratio="8 / 6"
          spinner-color="primary"
          spinner-size="82px"
        />
      </div>
      <div class="col-12 col-md-6">
        <div class="text-h2 text-bold">
          Know your buyer, <br />like you know your business.
        </div>
        <div class="q-mt-md">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem commodi
          excepturi enim, facere culpa sint quos eligendi corporis provident
          nisi accusantium deleniti magni aliquam officiis velit saepe corrupti
          voluptatum ut.
        </div>
      </div>
    </div>

    <div>
      <div class="q-pa-xl row">
        <div class="col-12 col-md-6">
          <div class="text-h2 text-bold">
            Know your buyer, <br />like you know your business.
          </div>
          <div class="q-mt-md">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem
            commodi excepturi enim, facere culpa sint quos eligendi corporis
            provident nisi accusantium deleniti magni aliquam officiis velit
            saepe corrupti voluptatum ut.
          </div>
        </div>
        <div class="col-12 col-md-6">
          <q-img
            src="~assets/priya.png"
            :ratio="8 / 6"
            spinner-color="primary"
            spinner-size="82px"
          />
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
  gap: 60px;
}

.centered-lorem {
  margin-top: 10px;
}
.centered-cols {
  text-align: center;
  color: rgba(44, 148, 204, 0.856);
}
.col {
  flex: 0 1 300px;
}
.btn-wrapper {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}
</style>
