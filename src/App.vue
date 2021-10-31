<template>
  <div id="app">
    <ProductList/>
    <button type="button" class="btn btn-primary" @click="getData">GET</button>
  </div>
</template>

<script>

import ProductList from './components/ProductList.vue'

export default {
  name: 'App',
  components: {
    ProductList
  },
  data(){
    return{
      film: {}
      
    }    
  },
  methods: {
    getData(){
      fetch(
        'https://api.themoviedb.org/3/movie/76341?api_key=95003f7d4b568b631f25e606a803207e'
        )
        .then(response => response.json())
        .then(data => {          
          this.film = data          
          console.log(this.film);
        })
      
    }
  }  
}
</script>

