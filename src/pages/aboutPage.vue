<template>
  <div class="q-pa-xl">
    <div class="row flex-center">
      <div class="text-h3 text-bold">Meet our beatiful team</div>
      <div class="text_one">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis
        laboriosam doloribus error eum perspiciatis rerum, totam neque sequi
        reiciendis officia sed amet blanditiis ipsam possimus, temporibus
        dignissimos quas? Vel, dicta!
      </div>
      <div>
        <div class="q-gutter-md">
          <q-carousel
            v-model="slide"
            transition-prev="scale"
            transition-next="scale"
            swipeable
            animated
            control-color="black"
            navigation
            padding
            arrows
            height="400px"
            class="bg-white text-black rounded-borders"
          >
            <q-carousel-slide name="boss" class="column no-wrap flex-center">
              <q-img
                src="~assets/rocky.png"
                ratio="16/9"
                spinner-size="82px"
                style="height: 300px; width: 300px"
              />
              <div class="q-mt-md text-center">
                <div class="text-bold">{{ Name }}</div>
                <div>{{ lorem }}</div>
              </div>
            </q-carousel-slide>
            <q-carousel-slide
              name="employee_1"
              class="column no-wrap flex-center"
            >
              <q-img
                src="~assets/emon.png"
                ratio="16/9"
                spinner-size="82px"
                style="height: 300px; width: 300px"
              />
              <div class="q-mt-md text-center">
                <div class="text-bold">{{ Name_1 }}</div>
                <div>{{ Employee_1 }}</div>
              </div>
            </q-carousel-slide>
            <q-carousel-slide name="employee_2" class="column no-wrap flex-center">
              <q-img
                src="~assets/rahul.png"
                ratio="16/9"
                spinner-size="82px"
                style="height: 300px; width: 300px"
              />
              <div class="q-mt-md text-center text-bold">
                <div>{{ Name_2 }}</div>
                <div>{{ Employee_2 }}</div>
              </div>
            </q-carousel-slide>
          </q-carousel>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      slide: ref("boss"),
      lorem: "CEO of the Company",
      Name: "Rocky",
      Name_1: "Emon",
      Name_2: "Rahul",
      Employee_1: "Employee of the Company",
      Employee_2: "Employee of the Company",
    };
  },
};
</script>

<style scoped>
.text_one {
  padding: 0 20%;
  margin: 10px;
}
</style>
