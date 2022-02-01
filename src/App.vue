<template>
    <MyBtn >BANANA</MyBtn>
    <MyBtn v-bind:color="color">BANANA</MyBtn>
    <MyBtn large color="orange" >APPLE</MyBtn>
    <MyBtn >BANANA</MyBtn>
    <MyList></MyList>
    <MyTab :tabList="tabList">
      <template v-slot:tabPanel-1> Content 1 </template>
      <template v-slot:tabPanel-2> Content 2 </template>
      <template v-slot:tabPanel-3> Content 3 </template>
      <template v-slot:tabPanel-4> Content 4 </template>
    </MyTab>
</template>

<script>
import MyBtn from '~/components/MyBtn'
import MyList from '~/components/MyList'
import MyTab from '~/components/MyTab'

export default { 
    components:{
        MyBtn,
        MyList,
        MyTab
    },
    data(){
        return{
            color:'#000',
            tabList: ["Tab 1", "Tab 2", "Tab 3", "Tab 4"],
        }
    }
}
</script>

<style>
</style>
