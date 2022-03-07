<template>
  <v-theme-provider dark>
    <base-section
      id="contatos"
      class="accent text-center"
      space="56"
    
    >
      <base-icon class="mb-8">
        mdi-card-account-phone
      </base-icon>

      <base-section-heading
        color="transparent"
        title="Contato"
      >
        Será um prazer poder atende-los! Estamos aguardando seu contato:
      </base-section-heading>
      
         <v-icon right>
          mdi-google-maps
        </v-icon>
        <b>Endereço:</b><br/><a href="https://goo.gl/maps/UMQRU2jfd1bj9R1M8" style="color:#FFFFFF">Rua Topázio, 567 - Aclimação -</a><br/>
        
        São Paulo - SP <br/><br/>


        <v-icon right>
          mdi-phone
        </v-icon>
        <b>Telefone / WhatsApp:</b><br/><a href="tel:+55-11-97096-2710" style="color:#FFFFFF">(11) 97096-2710</a> <br/>
        
      <div class="py-4" />

      <v-btn
        class="font-weight-bold"
        color="white"
        href="https://api.whatsapp.com/send/?phone=5511970962710"
        light
        min-width="168"
        target="_blank"
        x-large
      >
        Toque aqui para whatsapp

        <v-icon right>
          mdi-whatsapp
        </v-icon>
      </v-btn>
    </base-section>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'SectionNews',

    provide: {
      heading: { align: 'center' },
    },
  }
</script>
