<template >
  <q-card :style=mgtop flat bordered class="my-card flex flex-center">
    <q-card-section>
      <div class="text-h4 text-bold text-grey-8">Hospedagem {{ plano }}</div>
    </q-card-section>
    <q-card-section>
      <div style="color: #f30168" class="text-h3 text-bold flex flex-center">
        {{ valor }}
      </div>
    </q-card-section>

    <q-card-section class="q-pt-none column flex-center">
      <p class="space color">{{ terH }}</p>
      <p class="space color">{{ qua }}</p>
    </q-card-section>

    <q-separator style="width: 250px" inset />

    <q-card-section class="column flex-center">
      <p class="text-subtitle1 space ide">{{ qui }}</p>
      <p class="text-subtitle1 space ide">{{ sex }}</p>
    </q-card-section>

    <q-separator style="width: 250px" inset />

    <q-card-actions class="q-px-md">
      <q-btn
        unelevated
        style="background-color: #f30168; margin-top: 15px"
        size="lg"
        class="full-width text-white text-subtitle1 in"
        :label=btnplano
        :to=urlPlano

      />
    </q-card-actions>

    <q-card-section>
      <q-card-section class="section">
        <p class="vtg-title">Seu site em servidores <u>no</u></p>
        <p class="vtg-title">
          <u>{{ pais }}</u>
        </p>
      </q-card-section>
      <q-card-section class="section">
        <div class="row text-subtitle1 vtg-ctn">
          <p>✓</p>
          <p class="vtg">Servidores em nossos data center {{ dataCenter }};</p>
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
          <p class="vtg">
            {{ qtdFTP }} usuário de FTP para upload ou download;
          </p>
        </div>
        <div class="row vtg-ctn">
          <p>✓</p>
          <p class="vtg vtg-ctn">
            {{ qtdEmail }} contas de e-mails profissionais;
          </p>
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

      <div v-if="migra">
        <q-card-section class="section">
          <p class="vtg-title">{{ migraTitle }}</p>
        </q-card-section>
        <q-card-section class="section">
          <div class="row vtg-ctn">
            <p>{{ migraSimbol }}</p>
            <p class="vtg">{{ migraText }}</p>
          </div>
        </q-card-section>
      </div>

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
    valor: String,
    plano: String,
    terH: String,
    qua: String,
    qui: String,
    sex: String,
    mgtop: String,

    pais: String,
    dataCenter: String,
    qtdFTP: String,
    qtdEmail: String,
    migraSimbol: String,
    migraTitle: String,
    migraText: String,

    migra: Boolean,
    urlPlano: String,
    btnplano: String,

    hospe: {
      type: String,
      required: true,
    },
  },
});
</script>



<style scoped>
.my-card {
  /* height: 1262px; */
  width: 348px;
  border-radius: 5px;
  position:static;
  margin: 15px;
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
.ide {
  line-height: 1;
  color: #666666;
}

.color {
  color: #666666;
}
</style>
