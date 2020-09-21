<template>
    <div style="text-align: center;">
        <v-container>
            <font Face="TH SarabunPSK" style="font-size: 20px;">HELLO</font>
            <font Face="TH SarabunPSK" style="font-size: 25px;"><b>Friend</b></font>
            <hr>
            <br>
            <br>
        </v-container>
        <div class="box1" style="padding-top: 20px;padding-bottom: 20px;">
                <v-avatar size="120" style="background: #ffffff;">
                    <v-img src="images/p.png" width="30"></v-img>
                </v-avatar>
                <p style="font-size:15px;">
                    <font Face="TH SarabunPSK" style="font-size: 15px;">
                        Lorem ipsum dolor sit amet, 
                        consectetuer adipiscing elit, sed diam nonummy nibh euismod 
                        tincidunt ut laoreet dolore magna aliquam erat volutpat.
                        Lorem ipsum dolor sit amet, 
                        consectetuer adipiscing elit, sed diam nonummy nibh euismod 
                        tincidunt ut laoreet dolore magna aliquam erat volutpat.
                    </font>
                </p>
            </div>
            <br>
            <nuxt-link to="pages2">
                <v-btn color="indigo">Pages2</v-btn>
            </nuxt-link>
    </div>
</template>
<script>
export default {
    layout:"p2",
}
</script>
<style scoped>
    .box1 {
    background: #75b7cd;
    margin-left: auto;
    margin-right: auto;
  }
</style>