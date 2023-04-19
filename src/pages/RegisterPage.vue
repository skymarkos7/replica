<template>
  <q-page class="flex flex-center column">
    <TitlePlanComponent />

    <q-card-section style="" class="row">
      <q-card style="padding: 30px; max-width: 617px">
        <q-form class="q-gutter-md">
          <q-card-section
            style="margin-left: 0; line-height: 1"
            class="justify-start"
          >
            <p style="line-height: 1" class="text-h5 text-bold">
              Dados do seu site
            </p>
            <p style="line-height: 1">
              Informe seus dados pessoais para acesso à sua
            </p>
          </q-card-section>
          <label
            ><p style="margin-top: -20px">Nome completo</p>
            <q-input
              outlined
              v-model="ph"
              placeholder="Informe seu nome completo"
              :dense="dense"
            />
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
              type="email"
            >
            </q-input>
          </label>

          <label
            ><p>Senha</p>
            <q-input
              style="margin-bottom: 20px"
              type="password"
              outlined
              v-model="ph"
              hint="No mínimo 8 caracteres"
              :dense="dense"
            >
            </q-input>
          </label>
          <label
            ><p>Confirme sua senha</p>
            <q-input
              style="margin-bottom: 20px"
              outlined
              type="password"
              v-model="ph"
              :dense="dense"
            >
            </q-input>
          </label>

          <q-card-section style="margin-left: 0" class="justify-start">
            <p class="text-h5 text-bold">Dados do seu site</p>
          </q-card-section>
          <label for=""
            ><p>Nome do meu site</p>
            <q-input
              class="in"
              outlined
              hint="Exatamente igual o título do seu site"
              v-model="ph"
              placeholder="Meu site"
              :dense="dense"
            ></q-input>
          </label>
          <q-card-section style="margin: 10px" class="row flex justify-left">
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
          <q-card-section>
            <q-btn
              unelevated
              style="background-color: #f30168"
              size="lg"
              class="full-width text-white text-subtitle1 in"
              label="CRIAR CONTA"
              href="#/index"
            />
          </q-card-section>
        </q-form>
      </q-card>

      <PlanComponent
        v-if="planoh == 1"
        :valor="h1Valor"
        :plano="h1Plano"
        :terH="terHG"
        :qua="qua"
        :qui="qui1"
        :sex="sex1"
        :pais="paisUsa"
        :dataCenter="dataCenterUsa"
        :qtdFTP="ftpH1"
        :qtdEmail="emailH1"
        :mgtop="mgtop"
        :urlPlano="plano1"
        :btnplano="btnplano"
      />

      <PlanComponent
        v-if="planoh == 2"
        :valor="h2Valor"
        :plano="h2Plano"
        :terH="terHP"
        :qua="qua"
        :qui="qui2"
        :sex="sex2"
        :pais="paisBrasil"
        :dataCenter="dataCenterBrasil"
        :qtdFTP="ftpH2"
        :qtdEmail="emailH2"
        :migraTitle="migracaoTitle2"
        :migraSimbol="migracaoSimbol2"
        :migraText="migracaoText2"
        :migra="migrac"
        :urlPlano="plano2"
        :btnplano="btnplano"
      />

      <PlanComponent
        v-if="planoh == 3"
        :valor="h3Valor"
        :plano="h3Plano"
        :terH="terHP"
        :qua="qua"
        :qui="qui2"
        :sex="sex3"
        :pais="paisBrasil"
        :dataCenter="dataCenterBrasil"
        :qtdFTP="ftpH3"
        :qtdEmail="emailH3"
        :migraTitle="migracaoTitle2"
        :migraSimbol="migracaoSimbol2"
        :migraText="migracaoText2"
        :migra="migrac"
        :urlPlano="plano3"
        :btnplano="btnplano"
      />
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

      h1Valor: "Grátis",
      h2Valor: "R$499/mês",
      h3Valor: "R$999/mês",

      h1Plano: "1",
      h2Plano: "2",
      h3Plano: "3",
      // mgtop: "margin-top:-80px",

      terHG: "você não paga nada para usar",
      terHP: "cobrado mensalmente",
      qua: "sem taxa de setup",

      qui1: "ideal para quem está",
      sex1: "començando",
      qui2: "ideal para site com mais",
      sex2: "mais de 30k de visitas.",
      sex3: "mais de 60k de visitas.",

      paisBrasil: "Brasil",
      paisUsa: "Estados Unidos.",
      data: "Estados Unidos.",
      dataCenterBrasil: "São Paulo",
      dataCenterUsa: "americanos",

      ftpH1: "1",
      ftpH2: "10",
      ftpH3: "Ilimitados",

      emailH1: "1",
      emailH2: "30",
      emailH3: "Ilimitadas",

      migracaoTitle2: "Migração Gratuita",
      migracaoSimbol2: "✓",
      migracaoText2: "Migramos todos seus sites para nossos servidores;",

      migrac: true,

      plano1: "register/1",
      plano2: "register/2",
      plano3: "register/3",

      planoh: "",
      btnplano: "TROCAR PLANO",
    };
  },
  mounted: function () {
    this.planoh = this.$route.params.plano;
  },
});
</script>
