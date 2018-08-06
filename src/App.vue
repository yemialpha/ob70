<template>
  <v-app>
    <v-navigation-drawer
      persistent
      :mini-variant="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      enable-resize-watcher
      app
    >
      <v-list>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar
      dark
      app
      :clipped-left="clipped"
    >
      <v-toolbar-side-icon class="col"  @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title class="col" v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
     
    </v-toolbar>
    <v-content class="home">
      <router-view/>
    </v-content>
    <v-footer color="black" >
      <v-spacer></v-spacer>
      <span class="yel">&copy; 2018</span>
      <v-spacer></v-spacer>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: true,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'OB70.Inc'
    }
  },
  name: 'App'
}
</script>

<style scoped>
 .col{
   color: yellow;
 }
 .home{
   background-color: #181818;
 }
  .yel{
    color: yellow;
  }
</style>
