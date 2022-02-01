<template>
    <button v-on:click="add">add</button>
    <h1>{{print}}</h1>
    <h1>{{msg}}</h1>
    <button v-on:click="changtxt">changtxt</button>
    <h2 v-bind:class="{ active: isActive }" @click="activate">클릭</h2>
    <h3 v-bind:style="{color,fontSize}" @click="trans">클릭</h3>
    <h3 v-bind:style="fontStyle">클릭</h3>
    <h3 v-bind:style="[fontStyle,backgroundStyle]">클릭</h3>
</template>

<script>
import Fruits from '~/components/Fruits'

export default {
    data(){
        return {
            msg:'Hello',
            print:'hey whatup',
            isActive: false,
            color: 'red',
            fontSize: '30px',
            fontStyle: {
                color:'orange',
                fontSize: '20px'
            },
            backgroundStyle: {
                backgroundColor:'gray'
            },
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
        },
        activate(){
            this.isActive = true
            
        },
        trans (){
            this.color = 'blue',
            this.fontSize = '100px'
        }   
    }
}
</script>

<style>
    h1{color:skyblue;}
    .active{color:red;}
</style>
