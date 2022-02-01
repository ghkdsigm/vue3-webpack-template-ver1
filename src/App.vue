<template>
    <button v-on:click="add">add</button>
    <h1>{{print}}</h1>
    <h1>
        {{ msg.split('').reverse().join('') }}
    </h1>
</template>

<script>
import Fruits from '~/components/Fruits'

export default {
    data(){
        return {
            msg:'Hello',
            print:'hey whatup'
        }
    },
    computed:{
        printed : {
            get(){
                return this.print.split('').reverse().join('')
            },
            set(value){
                this.print = value
            }
        }        
    },
    methods:{
        add() {
            this.printed += '!!'
        }
    }
}
</script>

<style>
    h1{color:red}
</style>
