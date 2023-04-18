<template>
  <q-card style="margin:15px ;" flat bordered class="my-card flex flex-center">
    <q-card-section>
      <div class="text-h4 text-bold">Hospedagem 1</div>
      <div style="color: #f30168" class="text-h3 text-bold">Grátis</div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      você não paga nada para usar sem taxa de setup
    </q-card-section>

    <q-card-section>
    <q-separator style="width: 300px;" inset />
  </q-card-section>


    <q-card-section> Ideal para quem está começando. </q-card-section>

    <q-separator inset />

    <q-card-actions class="q-px-md">
      <q-btn
        unelevated
        style="background-color: #f30168"
        size="lg"
        class="full-width text-white in"
        label="ESCOLHER ESSE PLANO"
        to="/"
      />
    </q-card-actions>

    <q-card-section>
      <p class="text-h6">Seu site em servidores no Estados Unidos.</p>
      <p>
        ✓ ASP. ASP.NET 2.0/3.0/3.5/ e 4.0/4.5/4.5.1/4.5.2 (medium trust) ou PHP
        5.3, 5.4, 5.5, 5.6 e 7.0;
      </p>
      <p>✓ 1 usuário de FTP para upload ou download;</p>
      <p>✓ 1 contas de e-mails profissionais;</p>
      <p>✓ 1 contas de e-mails profissionais;</p>
      <p>✓ 1 subdomínio gratuito;</p>
      <p class="text-h6">Suporte 24 horas, 7 dias por semana grátis;</p>
      <p class="text-h6">Aplicativos disponíveis;</p>

      <p>
        ✓ ASP. ASP.NET 2.0/3.0/3.5/ e 4.0/4.5/4.5.1/4.5.2 (medium trust) ou PHP
        5.3, 5.4, 5.5, 5.6 e 7.0;
      </p>
      <p>✓ Wordpress;</p>
      <p>✓ Drupal;</p>
      <p>✓ Entre outros...</p>
      <p class="text-h6">Você ainda tem</p>
      <p>✓ Webmail RoundCube;</p>
      <p>✓ AntiSpam;</p>
      <p>✓ Painel de gerenciamento de DNS;</p>
      <p>✓ Painel de controle web;</p>
      <p>✓ Configurações de PHP personalizáveis;</p>
      <p>✓ Certificado SSL Grátis;</p>
      <p>✓ Transferência ilimitada.</p>
      <p>✓ Drupal;</p>
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
</style>
