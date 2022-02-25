<template>
  <div>
<Navbar/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from '../src/components/Navbar.vue'
export default {
  name:'App',
  components:{Navbar}
}
</script>
<style>
:root{
  --quasePreto: #181818;
  --quaseBranco:#f0f0f0;
  --pretoNavbar: #a5a5a536;
  --amareloQueimado: #E9B224;
  --pretoTransparente: rgba(0, 0, 0, 0.527);
}

@import url(https://fonts.google.com/specimen/Yatra+One?query=Yatra+One);

*{
  font-family: 'Yatra One', cursive;
  margin: 0;
  padding: 0;
}

nav{
  z-index: 999;
}

a{
  text-decoration: none;
  outline: none;
}

</style>
