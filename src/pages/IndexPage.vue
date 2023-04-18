<template>
  <q-page style="background-color: #fafafc" class="flex flex-center">
    <q-header style="background-color: #fafafc; border: none" elevated>
      <q-toolbar>
        <q-space></q-space>
        <q-btn
          flat
          round
          size="17px"
          class="text-bold"
          style="background-color: #d9d9d9; margin: 30px"
          label="J"
        />
      </q-toolbar>
      <q-toolbar-title>
        <img
          alt="Quasar logo"
          src="~assets/img/Logo.png"
          style="width: 200px; margin: 30px"
        />
      </q-toolbar-title>
    </q-header>

    <div>
      <h4 style="margin: auto; margin-bottom: 8px;" class="text-left text-bold">Olá João,</h4>
      <h6 style="margin: auto; margin-bottom: 25px; font-size: 1.1rem;" class="text-left text-grey-8">Seja bem vindo a sua conta de hospedagem</h6>
      <iframe
        width="1158"
        height="660"
        src="https://www.youtube.com/embed/Ywh8NVAHswU"
        title="Como criar um servidor no Discord? | Locaweb"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
      <p
              style="margin: auto; margin-bottom: 20px; font-size: 1rem; margin-top: 20px;"
              class="text-left "
            >
              Caso tenha alguma dúvida, <a style="color:black" href=""> visite nossa central de ajuda.</a>
    </p>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>
