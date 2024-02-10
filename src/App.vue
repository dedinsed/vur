<template>
  <div class="container">
  <h1>gggggg</h1>
     </Card>
     <div class="rows">
  <button v-on:click="addAnimal" type="button" class="btn btn-danger">Нажать</button>
     </div>
  </div>
</template>

<script>
import Card from './components/card.vue'

export default {
  name: 'App',
  components: {
    Card,
  },
  provide:{
    animal:"кот"
  },
  methods{
    addAnimal(){
      this.animal = 2
    }
  }
  }

</script>

<style>

</style>
