<template>
    <MyBtn >BANANA</MyBtn>
    <MyBtn v-bind:color="color">BANANA</MyBtn>
    <MyBtn large color="orange" >APPLE</MyBtn>
    <MyBtn >BANANA</MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'

export default { 
    components:{
        MyBtn
    },
    data(){
        return{
            color:'#000'
        }
    }
}
</script>

<style>
</style>
