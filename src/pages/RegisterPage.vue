<template>
  <q-page class="flex flex-center column">
    <TitlePlanComponent />

    <q-card-section style="max-width: 1600px" class="row">
      <q-card-section class="col">
        <q-form class="q-gutter-md">
          <label
            ><p>Nome completo</p>
            <q-input
              style="margin-bottom: 20px"
              outlined
              v-model="ph"
              placeholder="Informe seu nome completo"
              :dense="dense"
            >
            </q-input>
          </label>

          <label
            ><p>Celular</p>
            <q-input
              style="margin-bottom: 20px"
              outlined
              v-model="ph"
              placeholder="(99) 99999 - 0000"
              :dense="dense"
              mask="(##) ##### - ####"
            >
            </q-input>
          </label>

          <label
            ><p>E-mail</p>
            <q-input
              style="margin-bottom: 20px"
              outlined
              v-model="ph"
              placeholder="Informe seu e-mail"
              :dense="dense"
            >
            </q-input>
          </label>

          <label
            ><p>Senha</p>
            <q-input
              style="margin-bottom: 20px"
              outlined
              v-model="ph"
              hint="No mínimo 8 caracteres"
              placeholder="Seu e-mail"
              :dense="dense"
            >
            </q-input>
          </label>

          <label
            >Confirme sua senha
            <q-input
              style="margin-bottom: 20px"
              outlined
              v-model="ph"
              placeholder="Seu e-mail"
              :dense="dense"
            >
            </q-input>
          </label>
          <q-card-section>
            <p>Dados do seu site</p>
          </q-card-section>
          <label for=""
            >Nome do meu site
            <q-input
              class="in"
              outlined
              hint="Exatamente igual o título do seu site"
              v-model="ph"
              placeholder="Meu site"
              :dense="dense"
            ></q-input>
          </label>
          <q-card-section style="margin:10px;" class="row flex justify-left">
            <q-checkbox
              class="col"
              style="line-height: 1"
              keep-color
              v-model="igree"
              size="1.7rem"
              color="red"
            />
            <p class="col-11" style="line-height: 1">
              Ao concluir com seu cadastro você concorda com nossos e ooliticas
              de orivacidade.
            </p>
          </q-card-section>
        </q-form>
      </q-card-section>
      <PlanComponent />
    </q-card-section>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import PlanComponent from "../components/PlanComponent.vue";
import TitlePlanComponent from "../components/TitlePlanComponent.vue";

export default defineComponent({
  name: "RegisterPage",
  components: {
    TitlePlanComponent,
    PlanComponent,
  },
  data() {
    return {
      igree: false,
    };
  },
});
</script>
