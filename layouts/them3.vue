<template>
<v-app style="background: #FFFFFF;">
  <v-row>
    <v-col cols="12" sm="6" offset-sm="3">
      <v-card height="200px" style="background: #FFFFFF;">
        <v-card-title class="blue white--text">
          <span class="headline">Menu</span>

          <v-spacer></v-spacer>

          <v-menu bottom left>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                dark
                icon
                v-bind="attrs"
                v-on="on"
              >
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </template>

            <v-list>
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
                @click="goto(item)"
              >
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </v-card-title>

        <v-card-text style="color: #000;">
            <v-content>
                <nuxt />
            </v-content>

        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</v-app>
</template>

<script>
  export default {
    data: () => ({
      items: [
        { title: 'Home',path:'/Krunam/'},
        { title: 'Books',path:'/Krunam/books' },
        { title: 'Choose Program',path:'/Krunam/choose' },
        { title: 'About Me',path:'/Krunam/about' },
      ],
    }),
     methods:{
        goto(item){
            this.$router.push(item.path)
        },
     },
  }
</script>