<template>
  <q-page padding>
    <div class="q-pa-md flex flex-center" style="height: 100vh">
      <div class="q-pa-md" style="max-width: 400px; width: 100%">
        <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md">
          <q-input
            outlined
            type="text"
            v-model="name"
            label="Name *"
            rounded
            bg-color="green-1"
            lazy-rules
            :rules="[
              (val) => (val !== null && val !== '') || 'Please type your name',
            ]"
          />

          <q-input
            outlined
            type="number"
            v-model="age"
            label="Age *"
            rounded
            bg-color="green-1"
            lazy-rules
            :rules="[
              (val) => (val !== null && val !== '') || 'Please type your age',
              (val) => (val > 0 && val < 100) || 'Please type a real age',
            ]"
          />

          <q-toggle v-model="accept" label="I accept the license and terms" />

          <div>
            <q-btn label="Submit" type="submit" rounded no-cap color="green" />
            <q-btn
              label="Reset"
              type="reset"
              color="primary"
              flat
              class="q-ml-sm"
            />
          </div>
        </q-form>
      </div>
    </div>
  </q-page>
</template>

<script>
import { useQuasar } from "quasar";
import { ref } from "vue";

export default {
  setup() {
    const $q = useQuasar();

    const name = ref(null);
    const age = ref(null);
    const accept = ref(false);

    return {
      name,
      age,
      accept,

      onSubmit() {
        if (accept.value !== true) {
          $q.notify({
            color: "red-5",
            textColor: "white",
            icon: "warning",
            message: "You need to accept the license and terms first",
          });
        } else {
          $q.notify({
            color: "green-4",
            textColor: "white",
            icon: "cloud_done",
            message: "Submitted",
          });
        }
      },

      onReset() {
        name.value = null;
        age.value = null;
        accept.value = false;
      },
    };
  },
};
</script>
