<template>
  <q-page style="background-color: #fafafc">
    <q-card-section class="flex flex-center column justify-center">
      <img
        alt="Quasar logo"
        src="~assets/img/Logo.png"
        style="width: 200px; margin: 30px"
      />
      <p  class="text-h5 text-bold sub">Você está muito próximo de mudar a forma de</p>
      <p style="color: #f30168; margin-bottom:30px ;" class="text-h5 text-bold sub"><u>hospedar seu site</u></p>
      <p class="text-subtitle2">Escolha o seu plano</p>
    </q-card-section>

    <div class="flex flex-center">
      <PlanComponent />

      <PlanComponent />

      <PlanComponent />
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import PlanComponent from "../components/PlanComponent.vue";

export default defineComponent({
  name: "PlansPage",
  components: {
    PlanComponent
  },
});
</script>


<style scoped>
.sub{
  margin: 0 auto;
}
</style>
