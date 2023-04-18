<template>
  <q-page
    style="background-color: #fafafc"
    class="window-height window-width row justify-center items-center"
  >
    <div class="column justify-center items-center">
      <img
        alt="Quasar logo"
        src="~assets/img/Logo.png"
        style="width: 200px; margin: 30px"
      />
      <div class="row"></div>
      <div class="row">
        <q-card class="q-pa-lg shadow-1">
          <q-card-section class="text-center q-pa-none">
            <h4 style="margin: auto" class="text-left text-bold">
              Entre na sua conta
            </h4>
            <h6
              style="margin: auto; margin-bottom: 20px"
              class="text-left text-grey-8"
            >
              Para acessar sua conta informe seu e-mail e senha
            </h6>
          </q-card-section>
          <q-card-section>
            <q-form class="q-gutter-md">
              <label class="left"
                >E-mail
                <q-input
                  class="in"
                  style="margin-bottom: 20px"
                  outlined
                  v-model="ph"
                  placeholder="Seu e-mail"
                  :dense="dense"
                >
                </q-input>
              </label>

              <label for=""
                >Senha
                <q-input
                  class="in"
                  outlined
                  v-model="ph"
                  placeholder="Sua senha"
                  :dense="dense"
                ></q-input>
              </label>
            </q-form>
            <q-card-section class="text-center q-pa-none">
              <a style="text-decoration: none; font-size: 1rem" href="#"
                ><p class="text-right text-9 text-grey-8">
                  Esqueci minha senha
                </p></a
              >
            </q-card-section>
          </q-card-section>

          <q-card-actions class="q-px-md">
            <q-btn
              unelevated
              style="background-color: #f30168"
              size="lg"
              class="full-width text-white in"
              label="FAZER LOGIN"
              to="/"
            />
          </q-card-actions>
        </q-card>
      </div>
      <p style="margin: 30px; font-size: 1.3rem" class="text-grey-9 text-x10">
        Ainda não tem conta? <a style="color: #f30168" href="#/plans">Cadastre-se</a>
      </p>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "LoginPage",
  data() {
    return {
      email: "",
      password: "",
    };
  },
};
</script>

<style>
.q-card {
  height: 492px;
  width: 617px;
  border-radius: 5px;
}
.in {
  height: 80px;
}
</style>
