<template>
  <q-page >

    <TitlePlanComponent/>

    <p class="text-subtitle2 justify-center row">Escolha o seu plano</p>

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
import TitlePlanComponent from "../components/TitlePlanComponent.vue";

export default defineComponent({
  name: "PlansPage",
  components: {
    PlanComponent,
    TitlePlanComponent
  },
});
</script>


<style scoped>

</style>
