<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

const linksList = [
  {
    title: "Index",
    caption: "Repositório do projeto",
    icon: "code",
    target: "_self",
    link: "#",
  },
  {
    title: "login",
    caption: "chat.quasar.dev",
    icon: "link",
    target: "_self",
    link: "#/login",
  },
  {
    title: "cadastro",
    caption: "forum.quasar.dev",
    icon: "person",
    target: "_self",
    link: "#/register",
  },
  {
    title: "plans",
    caption: "@quasarframework",
    icon: "money",
    target: "_self",
    link: "#/plans",
  },
];

export default defineComponent({
  name: "MainLayout",

  components: {
  },

  setup() {

    return {

    };
  },
});
</script>
