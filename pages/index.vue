<template>
    <div id="app" class="flex flex-wrap list">
        <div class="w-1/4 list">
        <List 
            @chooseBeer="updateDetail"
            :beers="beers"
            :listName="beers"    
        />
        </div><div class="w-3/4 detail">
        <div class="top-detail w-full">

        </div>
        <h2><nuxt-child :key="$route.params.id"/></h2>
        </div>
    </div>
</template>
<script>
import axios from 'axios'
import List from '~/components/List'
import Detailview from '~/components/Detailview'
export default {
    data () {
        return{
            name: 'my-component',
            results: [],
            beers: [],
            beer_id: 0,
            beer_show: [],
            selected: null
        }
    },
    components: {
        List,
        Detailview  
    },
    created () {
        axios.get(`https://api.punkapi.com/v2/beers`)
                    .then(response => {
                        this.beers = response.data
                        console.log(this.results[0].link)
                    });
       
    },

    methods: {
        updateDetail(value){
            this.beer_show= value
           }
    }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Slab');
.detail {
    background-color: #F3F6E7;
}
.top-detail {
    background-image: url('http://rushriverbeer.com/wp-content/uploads/2015/04/OurBrews_Hearder_V21.jpg');
    height:20%;
}
</style>

    
