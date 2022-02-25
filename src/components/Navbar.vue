<template>
<header>
    <div class="navbar">
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
    background: var(--pretoNavbar);
    position: fixed;
    width: 100%;
}

.navbar{
    width: 80%;
    height: 60px;
    line-height: 60px;
    display: flex;
    justify-content: space-between;
    margin: auto;
}

h2{
    color: var(--amareloQueimado);
}

h3{
    color: #fff;
}
</style>