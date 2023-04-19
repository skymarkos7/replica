<template>
  <q-page style="background-color: #fafafc" class="flex flex-center">
    <div
      class="justify-between row"
      style="width: 100%; max-width: 1200px; margin: 0 auto"
    >
      <q-toolbar-title>
        <img
          alt="Quasar logo"
          src="~assets/img/Logo.png"
          style="width: 136px; margin: 30px"
        />
      </q-toolbar-title>
      <div class="column">
        <q-btn
          flat
          round
          size="17px"
          class="text-bold"
          style="
            background-color: #d9d9d9;
            margin-top: 10px;
            margin-right: 40px;
          "
          label="J"
          @click="logout()"
        />

        <a
          style="text-decoration: none; margin-top: 20px; margin-left: 10px"
          href="#/login"
          ><p v-if="sair">Sair</p></a
        >
      </div>
    </div>

    <div style="max-width: 900px" class="flex">
      <q-card-section class="justify-start column">
        <h4 style="margin-bottom: 8px" class="text-bold">Olá João,</h4>
        <h6
          style="margin-bottom: 25px; margin-top: 8px; font-size: 1.1rem"
          class="text-left text-grey-8"
        >
          Seja bem vindo a sua conta de hospedagem
        </h6>
      </q-card-section>
      <q-card-section class="flex flex-center justify-center">
        <iframe
          width="976"
          height="654"
          src="https://www.youtube.com/embed/Ywh8NVAHswU"
          title="Como criar um servidor no Discord? | Locaweb"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          allowfullscreen
        ></iframe>
      </q-card-section>
        <p style="font-size: 1rem; margin-top: 20px" class="text-left">
          Caso tenha alguma dúvida,
          <a style="color: black" href=""> visite nossa central de ajuda.</a>
        </p>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  data() {
    return {
      sair: false,
    };
  },
  methods: {
    logout() {
      if (this.sair == true) {
        this.sair = false;
      } else {
        this.sair = true;
      }

      /**
       * destruir sessão
       */
    },
  },
});
</script>
