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
            axios.get(`/${id}`)
            .then((response) => {
                this.Perso= response.data
            })
            .catch(error=>{})
}


}
}

</script>

<style scoped>

</style>