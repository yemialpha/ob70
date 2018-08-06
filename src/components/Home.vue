<template>
  <v-container fluid>
     <header class="v-header conta">
       <div class="fullscreen-video-wrap">
        <video height="70%" src="https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Video%202018-08-06%20at%205.15.03%20AM.mp4?alt=media&token=21f0e5d3-5399-4a1a-9847-e72d5847fcee" autoplay="true" loop="true"></video>
       </div>
       <div class="header-overlay">
         <div class="header-content">
              <v-container>
                <v-toolbar color="warning" white>
                  <v-toolbar-title> 
                   <v-btn outline color="black" large>Men Collecting</v-btn>
           <v-btn outline color="black" large>Women Collecting</v-btn>
           <v-btn outline color="black" large>Popular Collecting</v-btn>
                </v-toolbar-title>
              </v-toolbar>
              </v-container>
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
             <div
                id="e3"
                style="max-width: 400px; margin: auto;"
                class="grey lighten-3"
              >
                <v-flex xs12>
            <v-card color="purple" class="white--text">
              <v-layout row>
                <v-flex xs7>
                  <v-card-title primary-title>
                    <div>
                      <div class="headline">OB70.Inc</div>
                      <div>Handcrafted with care</div>
                    </div>
                  </v-card-title>
                </v-flex>
                <v-flex xs5>
                  <v-card-media
                    src="https://cdn.vuetifyjs.com/images/cards/halcyon.png"
                    height="125px"
                    contain
                  ></v-card-media>
                </v-flex>
              </v-layout>
              <v-divider light></v-divider>
              <v-card-actions class="pa-3">
                Coming Soon....
                <v-spacer></v-spacer>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
              </v-card-actions>
            </v-card>
          </v-flex>
             </div>
         </div>
       </div>
     </header>
  </v-container>
</template>
 <script>
     export default {
    data () {
      return {
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
    }
  }

 </script>
<style scoped>
  .v-progress-circular{
    margin: 1rem;
  }
.v-header{
  height: 100vh;
  display: flex;
  align-items: center;
  color: #fff;
}
.fullscreen-video-wrap{
  min-width: 100%;
  min-height: 100%;
}
.conta{
  max-width: 960px;
  padding-left: 1rem;
  padding-right: 1rem;
 
  text-align: center;
}
.header-overlay{
  height: 100%;
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
  background: #225470;
  z-index: 1;
  opacity: 0.8;
}
</style>
