<template>
  <section id="hero">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/bg.jpg')"
      class="white--text"
      gradient="to bottom, rgba(20, 20, 20, .1), rgba(0,0,0,.1)"
    >
      <v-container class="px-2 py-0">
        <v-responsive
          class="d-flex align-center mx-auto"
          height="50%"
          max-width="800"
          width="90%"
        >
        <br/><br/><br/>
        <v-card class="rounded-xl" color="#0000009D">
          <br/><br/>
          <v-row class="mx-6" align="center">
            <base-subheading
            size="text-h5"
            weight="regular"
            title="Borracharia Topázio, do seu lado sempre quando precisar!"/>
            <base-body >
              <p class="text-white">Prontos para atendê-los!</p>
              <p class="text-white">Atendemos de segunda à sábado das 08h às 22h. Domingos e feriados das 9h às 16h.</p> 
              <p class="text-white">Fazemos auto socorro.</p> 
              <p class="text-white">Trabalhamos com diversos serviços: Borracharia em geral, vulcanização de pneus cortados, venda de pneus meia vida, troca de lâmpadas e baterias.</p>
              <p class="text-white">Cuide de seu carro. Sua segurança e da sua família sempre em dia! </p>
              <p class="text-white">Estamos sempre ao seu lado! </p>
              <p class="text-white">Equipe Topázio Borracharia </p>
           </base-body>
          </v-row>
        </v-card>
        <br/><br/><br/><br/>
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
  export default {
    name: 'SectionHero',

    provide: {
      theme: { isDark: true },
    },

    computed: {
      minHeight () {
        const height = this.$vuetify.breakpoint.mdAndUp ? '50vh' : '25vh'

        return `calc(${height} - ${this.$vuetify.application.top}px)`
      },
    },
  }
</script>
<style type="text/css">
  rounded-card{
      border-radius:60;
  }
  p{
      color:white;
  }

</style>
