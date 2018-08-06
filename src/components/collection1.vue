<template>
  <v-layout row>
    <v-dialog v-model="dialog" transition="dialog-bottom-transition" :overlay="false">
      <v-btn color="black" large outline dark slot="activator"> <v-icon>backup</v-icon>Women Collections</v-btn>
      <v-card>
        <v-toolbar dark color="warning">
          <v-btn icon @click.native="dialog = false" dark>
            <v-icon>close</v-icon>
          </v-btn>
          <v-toolbar-title class="home" @click="open">  
        OB70.Inc Women Collections
        </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items>
            <v-btn dark flat @click.native="dialog = false">close</v-btn>
          </v-toolbar-items>
        </v-toolbar>
        <v-divider></v-divider>
        <v-content>
      <v-container>
           <v-toolbar color="pink" dark>
          <v-toolbar-title>  
        BEST COLLECTIONS
        </v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>
        <v-card-title></v-card-title>
        
        <v-layout wrap>
             <v-flex sm4>
               <v-card class="card1">
               </v-card>
           </v-flex>
           <v-flex sm6 offset-sm1>
               <v-card class="card1">
                   <h1>Coming Soon..... 
              <v-progress-circular
                :rotate="360"
                :size="100"
                :width="15"
                :value="value"
                color="warning"
              >
                {{ value }}
              </v-progress-circular>
           </h1>
               </v-card>
           </v-flex>
       </v-layout>
      </v-container>
    </v-content>
      </v-card>
    </v-dialog>
  </v-layout>
</template>
<script>
  export default {  
    data () {
      return {
        dialog: false,
        notifications: false,
        sound: true,
        widgets: false,
        paymentInfo: null,
        interval: {},
        value: 0
      }
    },
        beforeDestroy () {
      clearInterval(this.interval)
    },
    mounted () {
      this.interval = setInterval(() => {
        if (this.value === 100) {
          return (this.value = 0)
        }
        this.value += 10
      }, 1000)
    },
    methods: {
         open () {
        this.$router.push('/')
      }
  }
  }
</script>

<style scoped>
 .home{
   cursor: pointer;
   color: black;
 }
 .payment{
     background-color: rgb(39, 116, 141);
     border: 1px solid black;
     border-radius: 2px;
     margin-bottom: 10px;
     margin-right: 35%;
     margin-left: 35%;
     padding: 5px;

 }
 .card{
     background-color: lightgrey;
 }
 .card1{
     background-color: rgb(239, 244, 247);
     color: black;
     padding: 10px;
 }
</style>
