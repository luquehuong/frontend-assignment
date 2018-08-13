<template>
  <div class="container mx-auto max-w-full">
   <div class="flex">
    <div class="container w-1/3 list" >
       <input class="mt-10 ml-10" id="search" type="text" placeholder="Search for name" v-model="textSearch" @keyup.enter="search" >
       <ul id="listBeer">
        <li  v-for="beer in listBeer" :key="beer.id" @click="select=beer">
          <nuxt-link :to="`/${beer.id}`">
            {{ beer.name }}
          </nuxt-link>
        </li>

       </ul>

    </div>
    <div class="container mx-auto w-2/3 mt-20 listdetail">
           <div class="ml-10">
           <h1> {{ select.description }}</h1>
           </div>
    </div>
   </div>
  </div>
</template>

<script>
import axios from 'axios'
import Logo from '~/components/Logo.vue'


export default {

  components: {
    Logo
  },

  data() {
    return {
      listBeer: [],
      textSearch: '',
      select: '',
    }
  },
  created(){
    axios.get(`https://api.punkapi.com/v2/beers`)
    .then (response =>{
      this.listBeer = response.data
    })
  },
  methods: {
  search(){
       axios.get('https://api.punkapi.com/v2/beers?beer_name=' + this.textSearch).then(response => {
         this.listBeer = response.data
         if (this.listBeer.length === 0){document.getElementById('error').innerHTML = 'No Results Found'}
         else {document.getElementById('error').innerHTML = ' '}
       })
  },


  }


}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Bitter|Josefin+Sans');
@import url('https://fonts.googleapis.com/css?family=Lekton');
.container
{
  /* min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center; */
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
#search {
   width: 100%;
  font-size: 16px;
   padding: 12px 20px 12px 40px;
   border: 1px solid #ddd;
   border-radius: 5px;
}
#listBeer {
  list-style-type: none;
  padding: 0;
  margin: 0;
  color: black;
  display: block;
  font-size: 18px;
  padding: 12%;
}
.listdetail {
  font-family: 'Bitter', serif;
}
.list {
  font-family: 'Lekton', sans-serif;
}
li:hover{
  border: 2px dotted black;
}


</style>
