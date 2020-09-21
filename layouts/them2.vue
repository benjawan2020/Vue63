<template>
    <v-app style="background-color:#fff;">
        <v-row>
            <v-col cols="12" sm="6" offset-sm="3">
                <v-card height="auto">
                    <v-card-title class="bg1">
                        <span class="headline" style="text-shadow: 2px 2px #696C6D;">Wellcome<br>How Can<br>We Help Your?</span>
                        <v-spacer></v-spacer>
                        <v-avatar size="62">
                            <v-img src="images/icon.png"></v-img>
                        </v-avatar>
                    </v-card-title>

                    <v-card-text style="background-color:#fff;">
                        <nuxt/>
                    </v-card-text>

                </v-card>
            </v-col>
        </v-row>
    </v-app>
</template>
<style scoped>
  .bg1 {
    background: linear-gradient(to bottom left, #33e1fc 0%, #14bbf1 80%);
  }
</style>