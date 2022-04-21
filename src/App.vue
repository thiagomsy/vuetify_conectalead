<template>
  <v-app>
    <v-main class="grey lighten-2">
      <div style="height: 100%" class="d-flex flex-column flex-md-row justify-space-around align-center">
        <LeadCard
          name="Conversões"
          value="25 M"
          subtitle="Conversão é a ação do envio de qualquer formulário."
          icon_name="mdi-email-outline"
          icon_color="#1E93FF"
          class="my-2"
        />
        <LeadCard
          name="Leads"
          value="965321"
          subtitle=" Lead é um contato individual do cliente ao enviar formulários."
          icon_name="mdi-account-outline"
          icon_color="#B030FF"
          class="my-2"
        />
        <LeadCard
          name="Custo por lead"
          value="R$ 10"
          subtitle=" É o cálculo do investimento utilizado pela quantidade de leads gerados no período."
          icon_name="mdi-currency-usd"
          icon_color="#28CC56"
          class="my-2"
        />
      </div>
    </v-main>
  </v-app>
</template>

<script>
import LeadCard from "./components/LeadCard";

export default {
  name: "App",

  components: {
    LeadCard,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
#app {
  font-family: 'DM Sans', sans-serif;
}
</style>
