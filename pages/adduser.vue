<template>
    <form>
        <v-text-field
          v-model="username"
          ref="username"
          :counter="10"
          label="Username"
        ></v-text-field>
   
        <v-text-field
          v-model="password"
          label="Password"
        ></v-text-field>
     
        <v-select
          v-model="status"
          :items="items"
          label="status"
          data-vv-name="select"
        ></v-select>


      <v-btn
        class="mr-4"
        @click="save"
      >
        Save
      </v-btn>
      <v-btn @click="clear">
        clear
      </v-btn>
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
         username มีอยู่แล้ว
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            OK
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>

    </form>
</template>
<script>
export default {
    data(){
        return{
            username: '',
            password: '',
            status: '',
            dialog: false,
            items: ['admin','user','guest']
        }
    },
    methods: {
       async  save(){
            let student = {
            username: this.username,
            password: this.password,
            status: this.status
            }
            console.log('username:',this.username)
            console.log('password:', this.password)
        let res = await fetch('http://localhost:7000/insert', {
        method: 'post',
        headers: {
          'content-type': 'application/json',
        },
        body: JSON.stringify(student),
      })
      let data = await res.json()
      console.log('data',data.status)
      if(data.status == 'error'){
        this.dialog = true,
        this.$refs.username.focus()
      }
      
        }
    }
}
</script>