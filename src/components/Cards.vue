<template>
<div class="telacard" @click="teste(Perso.id)">
    <div class="card" v-for="teste in Perso" :key="teste.id">
        <img :src="teste.imageUrl" alt="">
        <p>{{teste.firstName}}</p>
    </div>
</div>
   
</template>

<script>
import axios from 'axios'

export default {
    name:'Cards',

    data() {
        return {
            Perso: [{
                id:'',
                firstName:"",
                lastName:"",
                fullName:"",
                family:"",
                title:"",
                imageUrl: "",
            }]
        };
    },
    props:{
        Personagens: Array
    },

    

    created(){
            axios.get('https://thronesapi.com/api/v2/Characters/')
            .then((response) => {
                this.Perso= response.data
                // console.log(this.Perso);
            });
    },

    methods: {
        teste(id) {
            this.$router.push({
                path: 'Personagem',
                query: { id },
            });;
        },
    },
}
</script>

<style scoped>

.card{
    display: flex;
    flex-direction: column;
    min-width: 10rem;
    height: 15rem;
    justify-content: center;
    align-items: center;
    padding: 1rem;
    flex: 1 1 10rem;
}

.telacard{
    /* display: grid;
    grid-template-columns: repeat(6, 1fr); */
    display: flex;
    flex-wrap: wrap;
}

img{
    max-width: 9rem;
    max-height: 9rem;
}

p{
    color: white;
    font-family: 'Yatra One', cursive;
    background-color: var(--pretoNavbar);
    padding: .5rem;
    margin-top: -2.5rem;
}

</style>