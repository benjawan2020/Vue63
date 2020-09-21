<template>
    <div style="text-align: center;">

        <div style="background: #45b4bd;">
            <v-container>
            <v-row style="padding: 10px;">
                <v-col cols="6" md="4">
                    <v-avatar size="90">
                        <v-img src="images/ben.jpg" width="300"></v-img>
                    </v-avatar>
                </v-col>
                <v-col cols="6" md="4">
                    <p style="text-align: justify;">
                        <font Face="TH SarabunPSK" style="font-size: 11px;"><b>
                            ชื่อ: เบญจวรรณ สิงหอำพล<br>
                            ชื่อเล่น: เบนเท็น<br>
                            แผนกวิชาเทคโนโลยีสารสนเทศ<br>
                        </b></font>
                          <v-btn  outlined color="#fff">แก้ไข</v-btn>
                          <v-btn  outlined color="#fff">ลบ</v-btn>
                    </p>
                </v-col>
            </v-row>
            </v-container>
        </div>
        <hr>
        <div class="card" style="background: #9fdad8;text-align: center;padding-top:10px;padding-bottom:70px;">
            <center>
                <v-card style="background: #fff;" width="350" height="45">
                     <v-row>
                <v-col cols="3">
                        <v-icon size="30" color="#99d9d9">mdi-clipboard-account</v-icon>
                </v-col>
                <v-col cols="6">
                    <p style="text-align: justify;color: #000;">
                        <font Face="TH SarabunPSK" style="font-size: 15px;"><b>เบญจวรรณ สิงหอำพล</b></font>
                    </p>
                </v-col>

                <v-col cols="3">
                     <v-icon size="30" color="#e5b509">mdi-exit-to-app</v-icon>
                </v-col>
            </v-row>
                </v-card><br>


                <v-card style="background: #fff;" width="350" height="45">
                     <v-row>
                <v-col cols="3">
                        <v-icon size="30" color="#99d9d9">mdi-cake-variant</v-icon>
                </v-col>
                <v-col cols="6">
                    <p style="text-align: justify;color: #000;">
                        <font Face="TH SarabunPSK" style="font-size: 15px;"><b>วันเกิด: 20/06/2543</b></font>
                    </p>
                </v-col>

                <v-col cols="3">
                    <v-icon size="30" color="#e5b509">mdi-exit-to-app</v-icon>
                </v-col>
            </v-row>
                </v-card><br>


                <v-card style="background: #fff;" width="350" height="45">
                     <v-row>
                <v-col cols="3">
                        <v-icon size="30" color="#99d9d9">mdi-cellphone-android</v-icon>
                </v-col>
                <v-col cols="6">
                    <p style="text-align: justify;color: #000;">
                        <font Face="TH SarabunPSK" style="font-size: 15px;"><b>088-422-7680</b></font>
                    </p>
                </v-col>

                <v-col cols="3">
                    <v-icon size="30" color="#e5b509">mdi-exit-to-app</v-icon>
                </v-col>
            </v-row>
                </v-card><br>

                <v-card style="background: #fff;" width="350" height="45">
                     <v-row>
                <v-col cols="3">
                        <v-icon size="30" color="#99d9d9">mdi-email</v-icon>
                </v-col>
                <v-col cols="6">
                    <p style="text-align: justify;color: #000;">
                        <font Face="TH SarabunPSK" style="font-size: 15px;"><b>ita5907@ccollege.ac.at</b></font>
                    </p>
                </v-col>

                <v-col cols="3">
                    <v-icon size="30" color="#e5b509">mdi-exit-to-app</v-icon>
                </v-col>
            </v-row>
                </v-card><br>
            </center>

             <nuxt-link to="pages3">
                <v-btn color="indigo">Pages3</v-btn>
            </nuxt-link>

        </div>
    </div>
</template>
<script>
export default {
    layout:"p3",
}
</script>
<style scoped>
    .card {
    margin-left: auto;
    margin-right: auto;
    padding-top: auto;
    padding-bottom: auto;
  }
</style>