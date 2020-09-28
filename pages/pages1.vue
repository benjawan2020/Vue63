<template>
    <div style="text-align: center;">
        <v-container>
            <font Face="TH SarabunPSK" style="font-size: 20px;">HELLO</font>
            <font Face="TH SarabunPSK" style="font-size: 25px;"><b>{{username}}</b></font>
            <hr>
            <br>
            <br>
        </v-container>
        <div class="box1" style="padding-top: 20px;padding-bottom: 20px;">
                <v-avatar size="120" style="background: #ffffff;">
                    <v-img src="images/p.png" width="30"></v-img>
                </v-avatar>
                <p style="font-size:15px;">
                    <font Face="TH SarabunPSK" style="font-size: 20px;text-align: justify;">
                        {{pre_name}}: {{username}} {{last_name}}<br>
                        ชื่อเล่น: {{nic_name}}
                    </font>
                </p>
            </div>
            <br>
            <nuxt-link to="pages2">
                <v-btn color="primary">Pages2</v-btn>
            </nuxt-link>
            <v-btn @click="LogOut" color="error"> LogOut</v-btn>
    </div>
</template>
<script>
export default {
    layout:"p2",
    data(){
        return{
            username: '',
            last_name: '',
            pre_name: '',
            nic_name: '',
        }
    },
async created() {
       let user = window.sessionStorage.getItem("user")
      // this.username=user
      let res = await fetch('http://localhost:7000/listuser?user='+ user)
      let data = await res.json()
      console.log(data.rows[0].first_name)
     this.username= data.rows[0].first_name
     this.last_name= data.rows[0].last_name
     this.pre_name= data.rows[0].pre_name
     this.nic_name= data.rows[0].nic_name
   },
          methods: {
           LogOut(){
               console.log('LogOut')
               window.sessionStorage.removeItem("user");
               this.$router.push('/')
           }
       }
}
</script>
<style scoped>
    .box1 {
    background: #75b7cd;
    margin-left: auto;
    margin-right: auto;
  }
</style>