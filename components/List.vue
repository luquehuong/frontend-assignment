<template>
    <div class="list_card">
        <div class="search_bar">
            <input id="search" type="text" placeholder="Search for name" v-model="textSearch" @keyup.enter="search" >
        </div>
        <div class="list_bar">
        <ul>
        <li v-for="beer in beers" :key="beer.id" @click="selectBeer(beer)">
            <nuxt-link :to="'/'+beer.id" class="no-underline">
            {{beer.name}}
            </nuxt-link>
        </li>
        </ul>
        </div>    
    </div>
</template>
<script>
import axios from "axios";
export default {
  props: ["beers"],
  data() {
    return {
      textSearch: "",
      listName: []
    };
  },
  methods: {
    selectBeer(beer) {
      this.$emit("chooseBeer", beer);
    },
    search() {
      axios
        .get("https://api.punkapi.com/v2/beers?beer_name=" + this.textSearch)
        .then(response => {
          this.beers = response.data;
          if (this.beers.length === 0) {
            document.getElementById("error").innerHTML = "No Results Found";
          } else {
            document.getElementById("error").innerHTML = " ";
          }
        });
    }
  }
};
</script>
<style scoped>
.search_bar {
    position: fixed;
    z-index: 9999;
}

.list_bar {
    position: relative;
    margin-top: 70px;
}
#search {
  width: 300px;
  height: 50px;
  border: 3px solid black;
  border-radius: 25px;
  padding: 3%;
  margin-bottom: 5%;
}
#search:focus {
    transform: scale(1.1);
    border: 5px solid black;
}
#search:hover {
    border: 5px solid black;
}
ul {
  position: relative;
  margin-top: 30px;
}
li {
  list-style-type: none;
  text-decoration: none;
  line-height: 1.8;
  margin-left: -10%;
  margin-top: 3% ;
}
li:hover {
  border-top: 2px solid black;
  border-bottom: 2px solid black;
  transform: scale(1.3);
  padding-left: 10%;
  font-size: 100%;
  z-index: 2;
}
li:active {
  color: #a5a0a0;
}
.list_card {
  
  padding-right: 5%;
  height: 100vh;
  overflow-y: scroll;
}
::-webkit-scrollbar {
    width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
    box-shadow: inset 0 0 5px grey; 
    border-radius: 10px;
}
 
/* Handle */
::-webkit-scrollbar-thumb {
    background: #E0E2E4; 
    border-radius: 10px;
    height: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
    background: grey; 
}
</style>


