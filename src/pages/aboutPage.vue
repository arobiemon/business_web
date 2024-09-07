<template>
  <div class="q-pa-xl">
    <div class="row flex-center">
      <div class="text-h3 text-bold">Meet our beautiful team</div>
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
            autoplay
            interval="4000"
          >
            <!-- Loop through the team array and create slides dynamically -->
            <q-carousel-slide
              v-for="(member, index) in team"
              :key="index"
              :name="member.name"
              class="column no-wrap flex-center"
            >
              <q-img
                :src="member.imgSrc"
                ratio="16/9"
                spinner-size="82px"
                style="height: 300px; width: 300px"
              />
              <div class="q-mt-md text-center">
                <div class="text-bold">{{ member.name }}</div>
                <div>{{ member.role }}</div>
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
    // Array of team members
    const team = ref([
      {
        name: "Rocky",
        role: "CEO of the Company",
        imgSrc:
          "https://passport-photo.online/images/cms/prepare_light_b364e3ec37.webp",
      },
      {
        name: "Emon",
        role: "Employee of the Company",
        imgSrc:
          "https://passport-photo.online/images/cms/prepare_light_b364e3ec37.webp",
      },
      {
        name: "Rahul",
        role: "Employee of the Company",
        imgSrc:
          "https://passport-photo.online/images/cms/prepare_light_b364e3ec37.webp",
      },
    ]);

    return {
      slide: ref("boss"),
      team,
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
