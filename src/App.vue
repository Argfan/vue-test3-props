<template>
  <div id="app">
    <!-- <ProductList/> -->
    <button type="button" class="btn btn-primary" @click="getData">GET</button>
    {{film.title}} <br>
    <img :src="'https://image.tmdb.org/t/p/w500'+film.poster_path" alt="">
  </div>
</template>

<script>

// import ProductList from './components/ProductList.vue'

export default {
  name: 'App',
  components: {
    // ProductList
  },
  data(){
    return{
      apiKey: 'api_key=95003f7d4b568b631f25e606a803207e',
      url1: 'https://api.themoviedb.org/3/movie/76341?',
      url2: 'https://api.themoviedb.org/3/genre/movie/list?',
      url3: '',
      film: {}      
    }    
  },
  methods: {
    getData(){
      fetch(
        this.url2+this.apiKey
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

