<template>
  
    <v-app-bar
      id="home-app-bar"
      app
      elevation="1"
      :height="barHeight"
      color="#2c70a7"
      >
        <home-menu/>

         <v-container>
        
          <v-row justify="center">
            
                <base-img  
                  class="mr-3" 
                  contain
                  max-width="200"
                  width="50%"
                  :src="require('@/assets/logo.png')"
                
                />
                 <v-divider 
                    vertical
                    inset
                    class="mr-3 hidden-xs-only"
                  />
                  <div class="mr-3 hidden-xs-only" style="text-align: center; padding-left: 16px; padding-right: 16px;">
                    <p class="text-white">
                      <v-icon left color="white">
                        mdi-google-maps
                      </v-icon>  
                      <b>Endereço</b><br/><a href="https://goo.gl/maps/UMQRU2jfd1bj9R1M8" style="color:#FFFFFF">Rua Topázio, 567 - Aclimação - SP</a><br/>
                      </p>
                  </div>
                  <v-divider 
                    vertical
                    inset
                    class="mr-3 hidden-xs-only"
                  />
                  <div class="mr-3 hidden-xs-only" style="text-align: center; padding-left: 16px; padding-right: 16px;">
                  <p class="text-white"  >
                    <v-icon left color="white">
                      mdi-phone
                    </v-icon>  
                    <b>Telefone / WhatsApp</b><br/> <a href="tel:+55-11-97096-2710" style="color:#FFFFFF">(11) 97096-2710</a> / <a href="tel:+55-11-94930-9390" style="color:#FFFFFF">(11) 94930-9390</a></p>
                  </div>
                
              
          </v-row>

          <v-row no-gutters>
            <v-col cols="12" class="text-center">
        
            </v-col>
          </v-row>
        </v-container>
          
         
         
           
        
    </v-app-bar>
 
</template>

<script>
  export default {
    name: 'HomeAppBar',

    data: () => ({
      drawer: null,
      items: [
        'Home',
        'Pro',
      ],
    }),

    components: {
      
      HomeMenu: () => import('@/layouts/home/menu'),
    },
    computed: {
      imageHeight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '100px'
          case 'sm': return '200px'
          case 'md': return '100px'
          case 'lg': return '100px'
          case 'xl': return '100px'
        }
      },
      imageWidth () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '240px'
          case 'sm': return '400px'
          case 'md': return '500px'
          case 'lg': return '500px'
          case 'xl': return '600px'
        }
      },
      barHeight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '90px'
          case 'sm': return '100px'
          case 'md': return '100px'
          case 'lg': return '100px'
          case 'xl': return '100px'
        }
      },
    }
  }
</script>

<style lang="sass">
  #home-app-bar
    .v-tabs-slider
      max-width: 24px
      margin: 2 auto

    .v-tab
      &::before
        display: none
</style>
