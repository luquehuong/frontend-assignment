<template>
    <div id="app" class="flex flex-wrap">
        <div class="w-1/3 px-10 pt-5 list">
        <List 
            @chooseBeer="updateDetail"
            :beers="beers"    
        />
        </div><div class="w-2/3">
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
*{
    font-family: 'Arvo', serif;
}   

</style>

    
