<template>
  <v-app class="bg">    
      <v-system-bar dark color="#46b5be">
            <v-icon>mdi-signal-cellular-outline</v-icon>
            <v-spacer></v-spacer>
            <v-icon>mdi-wifi-strength-4</v-icon>
            <v-icon>mdi-battery</v-icon>
            <span>12:30</span>
        </v-system-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    
  </v-app>
</template>
<style scoped>
  .bg {
    background: #46b5be;
  }
</style>

