<template>
    <div style="text-align: center;">
        <v-container>       
            <center>
                <v-icon size="120">mdi-angular</v-icon>
            </center>
            <h1>Welcome To My App</h1>
            <v-card-text>
       <v-form>
           <v-text-field label="User" auto-grow outlined rows="1" row-height="15" ref="username" v-model="username"></v-text-field>
           <v-text-field label="Password" auto-grow outlined rows="1" row-height="15" type="Password"  v-model="password"></v-text-field>
            <v-btn color="#ffffff" style="color:#000000;font-size:15px;" rounded @click="Signin">LOG IN</v-btn>
       </v-form>
       <p style="color: #000;">
           <b>
                CTC.<br>
                Chaiyaphum Technical College
           </b>
       </p>
       <center>
           
       </center>
        <v-row style="padding: 20px;paddin-top: 20px;">
            <v-col cols="4">
                <v-avatar size="40" style="background: #267ac2;">
                    <v-icon size="20" color="#fff">mdi-facebook</v-icon>
                </v-avatar>
            </v-col>

            <v-col cols="4">
                <v-avatar size="40" style="background: #75e4ff;">
                    <v-icon size="20" color="#fff">mdi-box</v-icon>
                </v-avatar>
            </v-col>

            <v-col cols="4">
                <v-avatar size="40" style="background: #ffbc06;">
                    <v-icon size="20" color="#fff">mdi-twitter</v-icon>
                </v-avatar>
            </v-col>
        </v-row>

         <nuxt-link to="pages1">
                <v-btn color="indigo">Pages1</v-btn>
            </nuxt-link>

     </v-card-text>
        </v-container>

        <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
     

      <v-card style="background: #D50000;">
        <v-card-title style="background: #D50000;">
          คำเตือน
        </v-card-title>

        <v-card-text>
         กรุณาตรวจสอบชื่อรหัสผ่าน
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="white"
            text
            @click="dialog = false"
          >
            I accept
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>

  <div class="text-center">
    <v-dialog
      v-model="dialog1"
      width="500"
    >

      <v-card>
        <v-card-title class="headline grey lighten-2">
          คำเตือน
        </v-card-title>

        <v-card-text>
         กรุณาตรวจสอบชื่อรหัสผ่าน
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialog1 = false"
          >
            OK
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>

  

    </div>
</template>
<script>
export default {
    data() {
        return {
            username: '',
            password: '',
            dialog: false,
            dialog1: false,
        }
    },
    methods: {   
      async  Signin(){
            let student = {
            username: this.username,
            password: this.password
            }
            console.log('username:',this.username)
            console.log('password:', this.password)
        let res = await fetch('http://localhost:7000/login', {
        method: 'post',
        headers: {
          'content-type': 'application/json',
        },
        body: JSON.stringify(student),
      })
      let data = await res.json()
      console.log('data',data.status)
      if(data.status == 'ok'){
          console.log('user=',data.row[0].username)
        //window.localStorage.setItem('user', JSON.stringify(res.data.user))// แบบนี้ เก็บถาวร
     window.sessionStorage.setItem("user", JSON.stringify(data.row[0].username)); // แบบนี้หาย เมื่อ restart หรือ ปิด  browser
        this.$router.push('/pages1') 
      }
      if(data.status == 'fail'){
       this.dialog = true
      }
      if(data.status == 'no'){
        this.$router.push('/') 
        this.username = '',
        this.password = '',
        this.dialog1 = true,
        this.$refs.username.focus()
      }

      
        }
    },
}
</script>
