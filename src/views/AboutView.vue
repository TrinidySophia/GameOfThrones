<template>
  <div class="about">

    <div class="h_1">
      <h1>About</h1>
    </div>

    <div class="h_2">
      <h1>This is an challenge for somes members of Tutilabs, to enable the development process. </h1>
    </div>

  </div>
</template>

<script>
export default {
  name:'About'
}
</script>

<style scoped>

.about{
  background-image: url('../assets/DragaoOfThrones.jpg');
}

h1{
  padding: 3rem;
  background-color: var(--pretoNavbar);
}

.h_1{
  color: #E9B224;
}

.h_2{
  color: white;
}

.about{
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  width: 50rem;
  padding: 5rem;
}
</style>