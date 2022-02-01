<template>
  <section v-if="fruits.length > 0">
    <h1>Fruitsd</h1>
    <ul>
      <li v-for="fruit in fruits" :key="fruit">
        {{fruit}}
      </li>
    </ul>
  </section>
  <section>
    <h1>Reverse Fruits</h1>
    <ul>
      <li v-for="fruit in reverseFruits" :key="fruit">
        {{fruit}}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fruits: [
        'Apple', 'Banana', 'Cherry'
      ]
    }
  },
  computed: {
    hasFruit(){
      return this.fruits.length > 0
    },
    reverseFruits(){
      return this.fruits.map(fruit => {
        return fruit.split('').reverse().join('')
      })
    }
  }
}
</script>