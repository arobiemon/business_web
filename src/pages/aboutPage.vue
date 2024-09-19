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
          "https://static.vecteezy.com/system/resources/previews/024/183/525/non_2x/avatar-of-a-man-portrait-of-a-young-guy-illustration-of-male-character-in-modern-color-style-vector.jpg",
      },
      {
        name: "Emon",
        role: "Employee of the Company",
        imgSrc:
          "https://static.vecteezy.com/system/resources/previews/024/183/525/non_2x/avatar-of-a-man-portrait-of-a-young-guy-illustration-of-male-character-in-modern-color-style-vector.jpg",
      },
      {
        name: "Rahul",
        role: "Employee of the Company",
        imgSrc:
          "https://static.vecteezy.com/system/resources/previews/024/183/525/non_2x/avatar-of-a-man-portrait-of-a-young-guy-illustration-of-male-character-in-modern-color-style-vector.jpg",
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
