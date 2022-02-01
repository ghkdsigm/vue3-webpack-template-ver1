<template>
    <button v-on:click="add">add</button>
    <h1>{{print}}</h1>
    <h1>{{msg}}</h1>
    <button v-on:click="changtxt">changtxt</button>
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
    watch:{
        msg(){
            console.log('msg', this.msg)
        }
    },
    methods:{
        add() {
            this.printed += '!!'
        },
        changtxt(){
            this.msg = 'good!!'
        }   
    }
}
</script>

<style>
    h1{color:red}
</style>
