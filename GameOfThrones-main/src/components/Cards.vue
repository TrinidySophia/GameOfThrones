<template>

<div class="telacard" >
    <div class="card" v-for="teste in Perso" :key="teste.id" @click="teste1(teste.id)">
        <img :src="teste.imageUrl" alt="">
        <p>{{teste.fullName}}</p>
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

    created(){
            this.getCards();
    },

    methods: {
        async getCards(){
            await axios.get('https://thronesapi.com/api/v2/Characters/')
            .then((response) => {
                this.Perso= response.data
            })
        },

        teste1(id) {
            this.$router.push({
                path: 'personagem',
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
    /* padding: 1rem; */
    flex: 1 1 13rem;
    cursor: pointer;
    margin: 1rem;
}

.card:hover{
    box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
    background-color: var(--pretoNavbar);
}

.telacard{
    /* display: grid;
    grid-template-columns: repeat(6, 1fr); */
    display: flex;
    flex-wrap: wrap;

}

img{
    max-width: 13rem;
    max-height: 12rem;
    border-radius: 3px;
}

p{
    color: white;
    font-family: 'Yatra One', cursive;
    background-color: var(--pretoNavbar);
    padding: .5rem;
    margin-top: -2.4rem;
}

</style>