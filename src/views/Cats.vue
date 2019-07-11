<template>
    <div>
        <h1>Cats For Adoption </h1>
       <petTable species="cats" :pets="cats"/>
    </div>     
</template>

<script>
// import cats from '../Data/cats'
import {mapState} from 'vuex'
import petTable from '../components/petTable'
export default {
    data(){
        return {
        }
    },
    components:{
        petTable
    },
    computed: {
        ...mapState([
            'cats'
        ])
    }
}

</script>