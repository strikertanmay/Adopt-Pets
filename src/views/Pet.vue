<template>
    <div>
      <h1>Pet Name : {{ animal.name }}</h1>
        <p>Age : {{ animal.age }} years</p>
        <p>Breed : {{ animal.breed}} </p>
    </div>   
</template>

<script>
// import cats from '../Data/cats'
import { mapState } from 'vuex'
export default {
    data(){
        return  {
            animal:{}
        }
    },
    computed: {
        ...mapState([
            'cats',
            'dogs'
        ])
    },
    mounted(){
        // const species = this.$route.params.species
        // const id = this.$route.params.id
        const animal = this[this.$route.params.species][this.$route.params.id]
        this.animal = animal       
    }
}
</script>