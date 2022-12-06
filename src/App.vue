<template>
  <div class="container">
    <HeaderTop restaurantName="Great Valley" subName="An Indian Restaurant" />

    <RestaurantItemsBox :items="items" />

</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import RestaurantItemsBox from './components/RestaurantItemsBox.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    RestaurantItemsBox
  },

  data(){

    return {
      items: []
    }

  },

  methods: {

    // promises

      async fetchItems(){
          const res = await fetch('https://nodejs-restaurant-portifolio.herokuapp.com/api')
          const data = await res.json()
          console.log( data )
          return data
      }


  },
  async created(){
    this.items = await this.fetchItems()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}

</style>
