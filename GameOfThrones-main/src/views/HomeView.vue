<template>

  <div class="nave">

    <div class="teste">
      <Cards/>
    </div>

  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'
import Cards from '../components/Cards.vue'

export default {
  name: 'HomeView',
  components: { Navbar, Cards },
}
</script>

<style scoped>

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
