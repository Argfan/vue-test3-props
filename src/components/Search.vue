<template>
  <div class="search flex">
    <input type="text" class="search" v-model="searchText" @input="$emit('search', searchText)">
    <!-- <button type="button" @click="$emit('search', searchText)">Найти</button> -->
  </div>
  <!-- <input type="text" class="search" @input="$emit('change', $event.target.value)"> -->
  
</template>
<script>

export default {
  name: "Search",
  // model: {
  //   prop: 'value',
  //   event: 'change'
  // },
  data(){
    return{
      searchText: ''
    }
    
  },
  methods: {
    
  }
  
}
</script>

<style lang="scss" scoped>
  input{
    height: 25px;
    margin-left: 40px;
  }
  button {
    background-color: rgb(221, 56, 56);
    color: #fff;
    border: none;
    border-radius: 4px;
    padding: 8px 14px;
    display: block;
    cursor: pointer;
    margin-left: 10px;
  }

</style>
