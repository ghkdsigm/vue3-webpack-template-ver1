<template>
    <button @click="handler">리스트생성</button>
    <ul>
        <li v-for="{id, name} in newFruits" :key="id" v-bind:id="id">
            {{name}}-{{id}}
        </li>
    </ul>
    
</template>

<script>
import shortid from 'shortid'

export default {
    data(){
        return {
           fruits:['apple','banana','cherry'],           
        }
    },
    computed:{
        newFruits(){
            return this.fruits.map(fruit => ({
                id:shortid.generate(),
                name:fruit              
            }))
        }
    },
    methods:{
        handler(){
            this.fruits.push('orange')
        }
    }
}
</script>

<style>
</style>
