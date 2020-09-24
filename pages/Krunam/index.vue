<template>
  <div style="text-align: center;">
    <v-container>
      <v-img class="img-doctor" src="images/doctor.png" width="200"></v-img>
      <h1>DOCTOR</h1>
      <h2>HELP</h2>
      <p style="font-size:12px;">Lorem ipsum dolor sit amet, 
          consectetuer adipiscing elit, sed diam nonummy nibh euismod 
          tincidunt ut laoreet dolore magna aliquam erat volutpat.
      </p>
      <nuxt-link to="/login">
        <v-btn color="#0072A6" rounded>SIGN UP</v-btn>
      </nuxt-link>
    </v-container>
  </div>
</template>
<style scoped>
  .img-doctor{
    margin-left: auto;
    margin-right: auto;
    margin-top: 100px;
  }
  h1{
    text-shadow: 2px 2px #696C6D;
  }
  h2{
    text-shadow: 2px 2px #696C6D;
  }
</style>