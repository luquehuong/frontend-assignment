<template>
  <div class="container mx-auto max-w-full">
   <div class="flex">
    <div class="container w-1/3 list" >
       <input class="mt-10 ml-10" id="search" type="text" placeholder="Search for name" v-model="textSearch" @keyup.enter="search" >
       <ul id="listBeer">
        <li  >

            {{ beer.name }}

        </li>

       </ul>

    </div>
    <div class="container mx-auto w-2/3 mt-20 listdetail">
           <div class="ml-10">
           <h1> {{ beer.description }}</h1>
           </div>
    </div>
   </div>
  </div>
</template>

<script>
import axios from 'axios'
  export default {
   async asyncData({ params, error }) {
      try {
        const {data} = await axios.get(`https://api.punkapi.com/v2/beers/${params.id}`)
        return {
          beer: data[0]
        }
      } catch (e) {
        error({ message: 'User not found', statusCode: 404 })
      }
    },
  }
</script>

<style scoped>

</style>
