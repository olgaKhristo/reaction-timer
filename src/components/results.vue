<template>
  <p>Reaction time: {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
props: ['score'],
data(){
    return{
        rank: null
    }
},
mounted(){
    if (this.score < 250) {
        this.rank = 'fast fingers'
    } else if(this.score < 400) {
        this.rank = 'rapid reflex'
    } else {
        this.rank = 'Snail pace'
    }
 }
}
</script>

<style>
.rank{
    font-size: 1.4rem;
    color:aqua;
    font-weight: bold;
}
</style>