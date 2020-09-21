<template>
    <div style="text-align: center;">
        <v-container>       
            <center>
                <v-icon size="120">mdi-angular</v-icon>
            </center>
            <h1>Welcome To My App</h1>
            <v-card-text>
       <v-form>
           <v-text-field label="User" auto-grow outlined rows="1" row-height="15" v-model="username"></v-text-field>
           <v-text-field label="Password" auto-grow outlined rows="1" row-height="15" type="Password"  v-model="password"></v-text-field>
            <v-btn color="#ffffff" style="color:#000000;font-size:15px;" rounded @click="signin">LOG IN</v-btn>
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
    </div>
</template>
<script>
export default {
    layout:"p1",
    data(){
        return{
            username: '',
            password: '',
        }
    },
    methods: {   
      async  signin(){
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
          this.$router.push('pages1')
      }else{
          this.$router.push('/')
      }
        }
    },
}
</script>
