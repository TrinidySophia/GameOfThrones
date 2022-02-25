<template>
<header>
    <div class="tronos">
        <router-link to="/">
            <h2>TutiOfThrones</h2>
        </router-link>
    </div>

    <div class="sobre">
        <router-link to="/About">
            <h3>About</h3>
        </router-link>
    </div>

</header>
    
</template>

<script>
export default {
    name:'Navbar'
}
</script>

<style scoped>
header{
    display: flex;
    background:var(--pretoNavbar) ;
    justify-content: space-between;
    padding: 1rem;
}

</style>