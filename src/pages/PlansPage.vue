<template>
  <q-page style="background-color: #fafafc">
    <q-card-section class="flex flex-center column justify-center">
      <img
        alt="Quasar logo"
        src="~assets/img/Logo.png"
        style="width: 200px; margin: 30px"
      />
      <p class="text-h6">Você está muito próximo de mudar a forma de</p>
      <p>hospedar seu site</p>
      <p>Escolha seu plano</p>
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
