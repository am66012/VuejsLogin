

<template>
  <v-content class="main_template"
    @click='isActive = !isActive'
    >
    <div id="app">
      <navigation></navigation>
      <!-- <navigation></navigation> -->
      <!-- <v-navigation-drawer dark></v-navigation-drawer> -->
      <!-- <navigation></navigation> -->
      <login></login>
      <login-form></login-form>
    </div>
  </v-content>
</template>

<script>
import Login from './components/Login.vue'
import LoginForm from './components/LoginForm.vue'
import Navigation from './components/Navigation.vue'
import 'vuetify/dist/vuetify.min.css'



export default {
  name: 'app',
  components: {
      'login':Login,
      'login-form' : LoginForm,
      'navigation' : Navigation,
    },
    
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding-top: 100px;
}

.main_toolbar{
  border-radius: 10px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

.main_template{
  height: 100%;
  /* background: #F7971E; 
  background: -webkit-linear-gradient(to right, #FFD200, #F7971E); 
  background: linear-gradient(to right, #FFD200, #F7971E);  */

  /* background: url(http://www.intrawallpaper.com/static/images/Minions-Despicable-Me-2-Wide-HD-Wallpapers1.jpg); */
  background: #34e89e;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #0f3443, #34e89e);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #0f3443, #34e89e); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}

.main_template1{
  height: 100%;
  background: #ee0979;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #ff6a00, #ee0979);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #ff6a00, #ee0979); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}
</style>
