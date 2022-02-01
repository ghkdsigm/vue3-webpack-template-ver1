<template>
    <button @click="handler">클릭</button>
    <template v-if="isShow">
        <ul>
            <li>1</li>
            <li>2</li>
        </ul>
    </template>
    <!--
    <div v-show="isShow">
        <ul>
            <li>1</li>
            <li>2</li>
        </ul>
    </div>
    -->
</template>

<script>
import Fruits from '~/components/Fruits'

export default {
    data(){
        return {
           isShow: true,
           count:0
        }
    },
    methods:{        
        handler (){
            this.isShow = !this.isShow
            this.count += 1
        }   
    }
}
</script>

<style>
</style>
