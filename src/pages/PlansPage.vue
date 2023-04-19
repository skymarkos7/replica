<template>
  <q-page >

    <TitlePlanComponent/>

    <p class="text-subtitle2 justify-center row">Escolha o seu plano</p>

    <div class="flex flex-center">
      <PlanComponent :valor="h1Valor" :plano="h1Plano" :terH="terHG" :qua="qua" :qui="qui1" :sex="sex1" />

      <PlanComponent :valor="h2Valor" :plano="h2Plano" :terH="terHP" :qua="qua" :qui="qui2" :sex="sex2" />

      <PlanComponent :valor="h3Valor" :plano="h3Plano" :terH="terHP" :qua="qua" :qui="qui2" :sex="sex3" />
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
  data() {
    return {
      h1Valor:  'Grátis',
      h2Valor:  'R$499/mês',
      h3Valor:  'R$999/mês',

      h1Plano:  '1',
      h2Plano:  '2',
      h3Plano:  '3',

      terHG: 'você não paga nada para usar',
      terHP: 'cobrado mensalmente',
      qua: 'sem taxa de setup',

      qui1: 'ideal para quem está',
      sex1: 'començando',
      qui2: 'ideal para site com mais',
      sex2: 'mais de 30k de visitas.',
      sex3: 'mais de 60k de visitas.',
    }
  }
});
</script>


<style scoped>

</style>
