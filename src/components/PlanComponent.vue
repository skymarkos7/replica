<template>
  <q-card style="margin: 15px" flat bordered class="my-card flex flex-center">
    <q-card-section>
      <div class="text-h4 text-bold text-grey-8">Hospedagem 1</div>
    </q-card-section>
    <q-card-section>
      <div style="color: #f30168" class="text-h3 text-bold flex flex-center">
        Grátis
      </div>
    </q-card-section>

    <q-card-section class="q-pt-none column flex-center">
      <p class="space color">você não paga nada para usar</p>
      <p class="space color">sem taxa de setup</p>
    </q-card-section>

    <q-separator style="width: 250px" inset />

    <q-card-section class="column flex-center">
      <p class="text-subtitle1 space ide">Ideal para quem está</p>
      <p class="text-subtitle1 space ide">começando.</p>
    </q-card-section>

    <q-separator style="width: 250px" inset />

    <q-card-actions class="q-px-md">
      <q-btn
        unelevated
        style="background-color: #f30168; margin-top: 15px"
        size="lg"
        class="full-width text-white text-subtitle1 in"
        label="ESCOLHER ESSE PLANO"
        to="register"
      />
    </q-card-actions>

    <q-card-section>
      <q-card-section class="section">
        <p class="vtg-title">Seu site em servidores <u>no</u></p>
        <p class="vtg-title"><u>Estados Unidos.</u></p>
      </q-card-section>
      <q-card-section class="section">
        <div class="row text-subtitle1 vtg-ctn">
          <p>✓</p>
          <p class="vtg">Servidores em nossos data center americanos;</p>
        </div>
        <div class="row text-subtitle1 vtg-ctn">
          <p>✓</p>
          <p class="vtg">
            ASP. ASP.NET 2.0/3.0/3.5/ e 4.0/4.5/4.5.1/4.5.2 (medium trust) ou
            PHP 5.3, 5.4, 5.5, 5.6 e 7.0;
          </p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg">1 usuário de FTP para upload ou download;</p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg vtg-ctn">1 contas de e-mails profissionais;</p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg vtg-ctn">1 contas de e-mails profissionais;</p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg">1 subdomínio gratuito;</p>
        </div>
      </q-card-section>
      <q-card-section class="section">
        <p class="vtg-title">Suporte 24 horas, 7 dias por semana grátis;</p>
      </q-card-section>
      <q-card-section class="section">
        <p class="vtg-title">Aplicativos disponíveis;</p>
      </q-card-section>
      <q-card-section class="section">
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg">Wordpress;</p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg">Drupal;</p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg">Entre outros...</p>
        </div>
      </q-card-section>
      <q-card-section class="section">
        <p class="vtg-title">Você ainda tem</p>
      </q-card-section>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Webmail RoundCube;</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">AntiSpam;</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Painel de gerenciamento de DNS;</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Painel de controle web;</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Configurações de PHP personalizáveis;</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Certificado SSL Grátis;</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Transferência ilimitada.</p>
      </div>
      <div class="row vtg-ctn">
        <p>✓</p>
        <p class="vtg">Drupal;</p>
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PlanComponent",
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
.my-card {
  height: 1262px;
  width: 348px;
  border-radius: 5px;
}

.space {
  margin: 0 auto;
}

.in {
  padding: 15px;
}
.vtg {
  width: 262px;
  margin-left: 5px;
  line-height: 1;
  color: #666666;
}
.vtg-ctn {
  line-height: 1;
}

.vtg-title {
  font-size: 1rem;
  font-weight: bold;
  color: #666666;
  line-height: 1.2;
  margin: 0 auto;
}
.section {
  padding: 8px;
}
.ide{
  line-height: 1;
  color: #666666;
}

.color{
  color: #666666;
}
</style>
