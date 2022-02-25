<template>

<div class="telacard">
    <div class="card">
        <div class="imagem">
            <img :src="Perso.imageUrl" alt="">
        </div>
        
        <div class="informacoes">
            <p>First Name: <span>{{Perso.firstName}}</span></p>
            <p>Last Name: <span>{{Perso.lastName}}</span></p>
            <p>Title: <span>{{Perso.family}}</span></p>
            <p>Family: <span>{{Perso.title}}</span></p>
        </div>
        
        
    </div>
</div> 

</template>

<script>
import axios from 'axios'
export default {
    name:'Personagens',
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
        this.getUSer();
            // axios.get(`https://thronesapi.com/api/v2/Characters/${this.$route.query.id}`)
            // .then((response) => {
            //     this.Perso= response.data
            // });
},

    methods:{
        getUSer(){
            axios.get(`https://thronesapi.com/api/v2/Characters/${this.$route.query.id}`)
            .then((response) => {
                this.Perso= response.data
                console.log(response.data);
            })
            .catch(error=>{})
}


}
}

</script>

<style scoped>

.telacard{
    background-image: url(../assets/GameOfThrones.jpg);
    width: 100%;
    height: 50rem;
}

img{
    border-radius: 3px;
    width: 20rem;
}

p{
    color: var(--amareloQueimado);
    font-size: 2.5rem;
}

span{
    color: #fff;
}

.card{
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 4rem;
}

.imagem{
    margin: 2rem;
}

.informacoes{
    margin: 2rem;
}

@media (max-width: 600px) {

.card{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
}
</style>