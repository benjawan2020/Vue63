<template>
  <v-app class="bg">    
      <v-system-bar dark color="#007ca4">
            <v-icon>mdi-signal-cellular-outline</v-icon>
            <v-spacer></v-spacer>
            <v-icon>mdi-wifi-strength-4</v-icon>
            <v-icon>mdi-battery</v-icon>
            <span>12:30</span>
        </v-system-bar>
      <div>
        <v-app-bar color="#007aa3">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>
          <font Face="TH SarabunPSK" style="font-size: 20px;">PHOTO &</font>
          <font Face="TH SarabunPSK" style="font-size: 20px;"><b>IMAGES</b></font>
      </v-toolbar-title>
    </v-app-bar>
      </div>

    <v-content>
        <nuxt />
    </v-content>
    
    <v-footer
    dark
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title style="background: #ffc807">
        <v-row style="padding: 50px;padding-top: 5px;">
            <v-col cols="4">
                <v-icon size="50">mdi-arrow-right-drop-circle-outline</v-icon>
            </v-col>

            <v-col cols="4">
                <v-icon size="50">mdi-arrow-right-drop-circle-outline</v-icon>
            </v-col>

            <v-col cols="4">
                <v-icon size="50">mdi-arrow-right-drop-circle-outline</v-icon>
            </v-col>
        </v-row>
      </v-card-title>
    </v-card>
  </v-footer>
    
  </v-app>
</template>
<style scoped>
  .bg {
    background: #007aa3;
  }
</style>

