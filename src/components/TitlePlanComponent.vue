<template>
  <q-card-section class="flex flex-center column justify-center">
      <img
        alt="Quasar logo"
        src="~assets/img/Logo.png"
        style="width: 200px; margin: 30px"
      />
      <p  class="text-h5 text-bold sub">Você está muito próximo de mudar a forma de</p>
      <p style="color: #f30168;" class="text-h5 text-bold sub"><u>hospedar seu site</u></p>
    </q-card-section>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "TitlePlanComponent",
  props: {
    title: {
      type: String,
      required: true,
    },

    caption: {
      type: String,
      default: "",
    },
  },
});
</script>



<style scoped>
.sub{
  margin: 0 auto;
}
</style>
