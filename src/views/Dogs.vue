<template>
    <div>
        <h1>Dogs For Adoption </h1>
        <petTable species="dogs" :pets="dogs"/>
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
            'dogs'
        ])
    }
}

</script>