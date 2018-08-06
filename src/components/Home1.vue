<template>
<v-container fluid>
   <v-container fluid>
        <v-carousel  class="back" hide-controls>
                <v-toolbar class="view" color="warning" white>
                  <Collections/>
                  <collections1/>
                  <collections2/>
              
              </v-toolbar>
    <v-carousel-item
    class="wid"
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >
    </v-carousel-item>
  </v-carousel>
   </v-container>

  <v-layout column>
      <v-toolbar color="#181818" dark>
        <v-toolbar-title class="feature">Featured Product</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>
      </v-toolbar>

      <v-card class="cards">
        <v-container
          fluid
          grid-list-md
        >
          <v-layout row wrap>
            <div
              v-for="card in cards"
              :key="card.title"
            >
              <v-card class="marg">
                    <div class="text-xs-center">
                  <img :src="card.src" alt="Smiley face" height="350">
                  </div>
                   <v-container
                    fill-height
                    fluid
                    pa-2
                  >
                   <v-layout fill-height>
                      <v-flex xs12 align-end flexbox>
                         <div class="headling white--text text-xs-center">
                            <v-btn fab color="indigo" dark>N 15,000</v-btn>
                        </div>
                      </v-flex>
                    </v-layout>
                  </v-container>
                <v-card-actions class="cards">
                       <v-layout fill-height>
                      <v-flex xs12 align-end flexbox>
                         <div class="headling white--text text-xs-center">
                           <featureproduct :card='card' />
                        </div>
                      </v-flex>
                    </v-layout>
                  <v-spacer></v-spacer>
                  <v-btn color="pink" icon>
                    <v-icon>favorite</v-icon>
                  </v-btn>
                  <v-btn color="pink" icon>
                    <v-icon>bookmark</v-icon>
                  </v-btn>
                  <v-btn color="pink" icon>
                    <v-icon>share</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </div>
          </v-layout>
        </v-container>
      </v-card>
  </v-layout>
    <v-layout column>
    <v-flex xs12 sm6 >
      <v-toolbar color="pink" dark>
        <v-toolbar-title>Featured Collections</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>
      </v-toolbar>

      <v-card class="cards">
        <v-container
          fluid
          grid-list-md
        >
          <v-layout row wrap>
            <div
              v-for="card in cards2"
              :key="card.title"
            >
              <v-card class="marg">
                  <div class="text-xs-center">
                  <img :src="card.src" alt="Smiley face" height="350">
                  </div>
                <v-card-actions class="cards">
                       <v-layout fill-height>
                      <v-flex xs12 align-end flexbox>
                         <div class="headling white--text text-xs-center">
                            <v-btn block outline color="info" dark>{{card.title}}</v-btn>
                        </div>
                      </v-flex>
                    </v-layout>
                  <v-spacer></v-spacer>
                  <v-btn color="info" icon>
                    <v-icon color="black">favorite</v-icon>
                  </v-btn>
                  <v-btn color="info" icon>
                    <v-icon color="black">bookmark</v-icon>
                  </v-btn>
                  <v-btn color="info" icon>
                    <v-icon color="black">share</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </div>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>

</v-container>
</template>

<script>
import Collections from './collection.vue'
import Collections1 from './collection1.vue'
import Collections2 from './collections2.vue'
import featureproduct from './featureproduct.vue'
  export default {
    components: {Collections, Collections1, Collections2, featureproduct},
    data () {
      return {
        items: [
          {
            src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.15.41%20AM.jpeg?alt=media&token=4eaac40e-d2b6-49fc-bc3e-51d1fbe9f0ba'
          },
          {
            src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.15.04%20AM.jpeg?alt=media&token=c93ddcac-23aa-4bf0-8367-9a382866c30a'
          },
          {
            src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.15.40%20AM.jpeg?alt=media&token=2519d521-eec3-4dd7-be55-e07c53d33360'
          },
          {
            src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.15.42%20AM.jpeg?alt=media&token=2a0c2ee2-55a7-4b9e-a0d9-ec24c724cba3'
          }
        ],
         cards: [
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.50%20AM.jpeg?alt=media&token=ea41579a-1566-409b-9517-67048b25c941', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.49%20AM.jpeg?alt=media&token=be1ff917-d09c-4e39-ba63-3f90fccd05db', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.51%20AM%20(1).jpeg?alt=media&token=dba9527b-13b6-4ac7-9968-5f2aee67a9ef', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.51%20AM%20(2).jpeg?alt=media&token=f9088799-9940-4d26-b1bd-1ec26b3bd752', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.51%20AM.jpeg?alt=media&token=de809247-5a20-46e4-9108-975251356bb1', flex: 6 }
      ],
         cards2: [
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.15.40%20AM%20(1).jpeg?alt=media&token=4b9e78d0-7ee7-49c6-95c7-fa81e7290ef0', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.15.43%20AM%20(1).jpeg?alt=media&token=a06aba98-daea-4114-995a-2e30cc1391dd', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.46%20AM.jpeg?alt=media&token=1b4def5b-8f28-4d9c-8b6b-561c3f98b2cc', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.50%20AM%20(1).jpeg?alt=media&token=feaaf158-7480-4ed3-9f96-8fb2b91d1856', flex: 6 },
        { title: 'Handcrafted with care', src: 'https://firebasestorage.googleapis.com/v0/b/ob70-72eee.appspot.com/o/WhatsApp%20Image%202018-08-06%20at%205.17.52%20AM.jpeg?alt=media&token=195dd75c-f7db-4c0e-8c55-61a62717c1da', flex: 6 }
      ]
      }
    }
  }
</script>
<style scoped>
.back{
    margin-bottom: 70px;
}
.feature{
    color: yellow;
}
.cards{
    background-color: #181818;
}
img{
    flex: 1;
}
.marg{
  margin: 20px;
}
 @media screen and (max-width: 480px) {
    .view{
        display: none;
    }
    .back{
      width: 100%;
    }
    .wid{
      width: 100%;
    }
    .marg{
      justify-content: center;
      align-items: center; 
    }
 
}
</style>
