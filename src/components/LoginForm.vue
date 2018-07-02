<template>
  <v-layout>
    <v-flex dark xs12 sm6 offset-sm3>
      <v-card class="Card-main">
        <v-form v-model="valid">
          <v-flex class="flex_inside">
            <v-text-field class="text_field"
              v-model="name"
              :rules="nameRules"
              :counter="10"
              label="Name"
              required
            ></v-text-field>
            <v-text-field class="text_field"
              v-model="email"
              :rules="emailRules"
              label="E-mail"
              required
            ></v-text-field>
              <v-btn class="submit_button"
              color="cyan darken-2" 
              @click='isActive = !isActive'
              v-on:click="toggle" 
              >
              SUBMIT
              </v-btn>
          </v-flex>
        </v-form>
      </v-card> 
    </v-flex>
  </v-layout>
</template>
<script>
let btn = document.querySelector('submit_button');
export default {
    data: () => ({
      valid: false,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => v.length <= 10 || 'Name must be less than 10 characters'
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
      ]
    }
    ),
    data:{
      isActive : true,
    },
    methods: {
      toggle : function(event){
        if(isActive){
          btn.classList.toggle("main_template1");
        }else{
          btn.classList.toggle("main_template");
        }
      }
    }
}
</script>
<style>
.flex_inside{
  margin-top:5px;
  padding: 8%;
  /* box-shadow: 5px 5px grey; */
  /* padding-top: 100px; */
  border: 0.1px solid grey;
  background: white;
  border-radius: 20px;
}

.submit_button{
  color:azure;
  border-radius: 15px;
}

.Card-main{
  border-radius: 20px;
}

/* .text_field{
  
} */
/* .main_layout{
  
} */
</style>

