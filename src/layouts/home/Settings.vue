<template>
  <v-menu
    v-model="menu"
    :close-on-content-click="true"
    bottom
    left
    max-width="100%"
    min-width="320"
    offset-x
    offset-y
    origin="top right"
    transition="scale-transition"
  >
    <template #activator="{ attrs, on }">
      <v-card
        id="settings"
        class="py-2 px-4"
        color="#498300"
        dark
        flat
        style="position: fixed; top: 100px; right: -35px;"
        width="220"
        v-bind="attrs"
        v-on="on"
      >
        <v-icon large>
          mdi-whatsapp
        </v-icon>
        Atendimento Já
      </v-card>
    </template>

    <v-card class="py-2">
      <br/>
      <base-title
        align="center"
        title="Contatos"
        space="0"
      />

      <v-card-text>
        <v-item-group
         
          class="d-flex justify-center"
        >
        </v-item-group>

        <v-divider class="my-6" />


       <div
          class="mr-4"
         
        >
          <v-icon left>
            mdi-phone
          </v-icon>
          <a href="tel:+55-11-97096-2710">(11) 97096-2710  / <a href="tel:+55-11-94930-9390">(11) 94930-9390</a></a>
        </div>

        <v-divider class="my-6" />

        <base-btn
          block
          href="https://api.whatsapp.com/send/?phone=5511970962710"
          class="mb-6"
          color="black"
          outlined
          target="_blank"
        >
        <v-icon left>
            mdi-whatsapp
          </v-icon>
          Whatsapp
        </base-btn>
         
      </v-card-text>
    </v-card>
  </v-menu>
</template>

<script>
  export default {
    name: 'HomeSettings',

    data () {
      return {
        colors: [
          this.$vuetify.theme.currentTheme.primary,
          '#9368e9',
          '#F4511E',
        ],
        menu: false,
      }
    },

    computed: {
      currentThemePrimary: {
        get () {
          return this.$vuetify.theme.currentTheme.primary
        },
        set (val) {
          const target = this.$vuetify.theme.isDark ? 'dark' : 'light'

          this.$vuetify.theme.themes[target].primary = val
        },
      },
    },
  }
</script>
