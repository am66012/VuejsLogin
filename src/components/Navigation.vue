<template>
    <v-layout>  
    <v-layout id="app1">
        <v-navigation-drawer
          v-model="drawer"
          temporary
          absolute
          >
          <v-list class="pa-1">
          <v-list-tile avatar>
          <v-list-tile-avatar>
          </v-list-tile-avatar>
          <v-list-tile-content>
            <v-list-tile-title>John Leider</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
      <v-list class="pt-0" dense>
        <v-divider></v-divider>
        <v-list-tile v-for="item in items" :key="item.title">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
      </v-navigation-drawer>
      </v-layout>
      <v-layout>
      <v-toolbar class="main_toolbar" color="white" absolute card light xs12 sm12>
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title color="orange"><i class="fa fa-lemon-o" aria-hidden="true"></i>&nbsp;Demo App</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat>Login&nbsp;<i class="fa fa-sign-in" aria-hidden="true"></i></v-btn>
          <v-btn flat>Sign Up&nbsp;<i class="fa fa-user-plus" aria-hidden="true"></i></v-btn>
          <v-btn flat>Need Help!&nbsp;<i class="fa fa-ambulance" aria-hidden="true"></i></v-btn>
        </v-toolbar-items>
      </v-toolbar>
      </v-layout>
      </v-layout>
</template>
<script>
export default {
    name:'app1',
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' }
        ]
      }
    },
}
</script>

