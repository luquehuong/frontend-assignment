<template>
    <div>
        <Detailview :beer_show="beer_show" />
    </div>
</template>
<script>
import axios from 'axios'
import Detailview from '~/components/Detailview'
export default {
    data( ) {
        return{
           id: this.$route.params.id,
           beer_show: [] 
        }
    },
    components: {
        Detailview  
    },  
    created () {
        axios.get(`https://api.punkapi.com/v2/beers/${this.id}`)
                    .then(response => {
                        this.beer_show = response.data[0]
                        console.log(this.results[0].link)
                    });
       
    }
}
</script>

