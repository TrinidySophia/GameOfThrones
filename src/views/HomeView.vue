<template>
<div class="nave">
<!-- <Navbar/> -->
<!-- <Cards/> -->
  <div class="teste" :v-for="teste in Personagens">
    <Cards :Personagens="Personagens"/>
  </div>
  
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'
import Cards from '../components/Cards.vue'
import axios from 'axios'

export default {
  name: 'HomeView',
  components: { Navbar, Cards },
  data() {
    return {
      Personagens: [],
    };
  },

  mounted(){
        this.teste()
    },

    methods:{
        async teste(){
           const response = await axios.get('https://thronesapi.com/api/v2/Characters/')
           .then ((response) => this.Personagens = response.data)
            }
        }

  // props:{
  //   Personagens: Array
  // }
}
</script>

<style scoped>
/* *{
  background-image: url("../assets/GameOfThrones.jpg") ;
} */

.home{
 background-image: url("../assets/game-of-thrones-zombies-night-king-art 1.png");
 background-repeat: no-repeat;
position: absolute;
}

.nave{
  background-image: url("../assets/game-of-thrones-zombies-night-king-art 1.png");
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  padding-top: 4rem;
}
</style>
