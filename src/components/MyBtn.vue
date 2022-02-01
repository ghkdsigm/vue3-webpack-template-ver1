<template>
  <div class="btn" v-bind:style="{backgroundColor:color}" v-bind:class="{large}">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props:{
    color:{
      type: String,
      default:'gray'
    },
    large:{
      type: Boolean,
      default: false,
    }
  }
}
</script>

<style scoped lang="scss">
  .btn {
    display:inline-block;
    padding:5px 15px;
    margin: 15px;
    color:#fff;
    border-radius: 15px;
    &.large {
      font-size:25px;
      padding:10px 20px;
      color:royalblue;
    }
  }
</style>