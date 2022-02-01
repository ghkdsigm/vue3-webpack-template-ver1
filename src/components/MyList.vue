<template>
  <ul class="list">
    <li v-for="fruit in fruits" :key="fruit">
      {{fruit}}
    </li>
  </ul>
</template>

<script>
export default {
  data(){
    return {
      fruits : ['banana','apple','cherry','mellon']
    }
  }  
}
</script>