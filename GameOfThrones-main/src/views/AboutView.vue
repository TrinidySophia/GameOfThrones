<template>
  <div class="about">

    <div class="quadro">
      <div class="h_1">
        <h1>About</h1>
      </div>

      <div class="h_2">
        <h1>This is an challenge for somes members of Tutilabs, to enable the development process. </h1>
      </div>
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
  background-repeat: no-repeat;
  background-position: center;
  /* width: 100%; */
}

.h_1{
  color: var(--amareloQueimado);
}

.h_2{
  color: white;
}

.about{
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  padding: 5rem;
  width: 90%;
  min-height: 40rem;
}

.quadro{
  padding: 3rem;
  background-color: var(--pretoTransparente);
  border-radius: 10px;
  width: 60rem;
}
</style>