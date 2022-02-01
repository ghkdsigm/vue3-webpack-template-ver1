<template>
    <button @click="message ='good?'">click</button>
    <h2>app{{message}}</h2>
    <Parent />    
</template>

<script>
import Parent from '~/components/Parent'
import { computed } from 'vue'

export default { 
    components:{
        Parent
    },
    data(){
        return{
            message:'Hello World',
           
        }
    },
    provide(){
        return{
            msg:computed(() => {
                return this.message
            })
        }
    }
}
</script>

<style>
</style>
