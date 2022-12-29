<template>
  <p>Reaction Time : {{ points }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
import { thisExpression } from '@babel/types';

export default {
    props: ['points'],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        //Ranks
        if(this.points < 250){
            this.rank = 'Faster than Light'
        }else if(this.points < 400){
            this.rank = 'Cat-like Reflexes'
        }else{
            this.rank = 'Snail pace... needs improvement'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }   

</style>