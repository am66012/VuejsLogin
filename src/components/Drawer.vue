
<template>
    <v-layout wrap height="200px">
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
</template>
<script>
export default {
    
}
</script>
<style>
.nav_layout{
    height:100%;
}
</style>




      