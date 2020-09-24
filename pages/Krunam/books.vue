<template>
    <div>
        <v-container>
            <v-card style="background-color:#fff;">
                <v-list-item three-line>
                    <v-list-item-content>
                        <div style="color: #0072A6;">DOCTOR LOREM</div>
                        <v-list-item-subtitle style="color: #696C6D;font-size:6px;">
                            Lorem ipsum dolor sit amet, 
                            consectetuer adipiscing elit, sed diam nonummy nibh euismod 
                            tincidunt ut laoreet dolore magna aliquam erat volutpat.
                        </v-list-item-subtitle>
                            <v-spacer></v-spacer>
                        <v-list-item-subtitle style="color: #696C6D;font-size:6px;">
                            Lorem ipsum dolor sit amet, 
                            consectetuer adipiscing elit, sed diam nonummy nibh euismod 
                            tincidunt ut laoreet dolore magna aliquam erat volutpat.
                        </v-list-item-subtitle>
                    </v-list-item-content>
                        <v-list-item-avatar tile size="90" style="padding-top: 40px;">
                            <v-img 
                            src="images/doctor1.png">
                            </v-img>
                        </v-list-item-avatar>
                </v-list-item>

                    <v-card-actions>
                        <v-btn rounded color="#0072A6" dark>LOREM IPSUM</v-btn>
                    </v-card-actions>
                    <p style="color: #696C6D;font-size:6px;padding: 10px;">
                        Lorem ipsum dolor sit amet, 
                        consectetuer adipiscing elit, sed diam nonummy nibh euismod 
                        tincidunt ut laoreet dolore magna aliquam erat volutpat.
                    </p>
            </v-card>

                <h4>LOREM IPSUM</h4>
                <p style="font-size: 8px;">
                    Lorem ipsum dolor sit amet, 
                    consectetuer adipiscing elit, sed diam nonummy nibh euismod 
                    tincidunt ut laoreet dolore magna aliquam erat volutpat.
                </p>

                <v-row justify="center">
                    <v-date-picker v-model="picker" color="green lighten-1" header-color="green lighten-1"></v-date-picker>
            </v-row>
            <br>
                    <div style="text-align: center;">
                        <v-btn rounded color="#0072A6" dark>BOOK APPOINTMENT</v-btn>
                    </div>
        </v-container>
    </div>
</template>
<script>
export default {
    data(){
        return{
            picker: new Date().toISOString().substr(0, 10),
        }
    }
}
</script>