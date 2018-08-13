<template>
    <div class="detail_bar pr-10 flex flex-wrap">
        <div class="img_bar w-1/3 -mt-16">
            <img :src="beer_show.image_url" class="ml-auto">
        </div>
        <div class="info_bar w-2/3 pt-10">
            <h1 class="text-left">{{beer_show.name}}</h1>
            <h5 class="text-left pb-10">{{beer_show.tagline}}</h5>
            <h4 class="pb-3">{{beer_show.description}}</h4>
            <div class="mb-3 p-3 flex flex-wrap list_wrap">
                <div v-for="item in beer_show.food_pairing" :key="item" class="w-full text-base list_box p-2">{{item}}</div>
            </div>
            <h4 class="tips">"{{beer_show.brewers_tips}}"</h4>
            <h1 class="ml-atuo name">{{beer_show.contributed_by}}</h1>
        </div>
    </div>
</template>
<script>
export default {
  props: ["beer_show"]
};
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Indie+Flower');
*{
    color: #42372b;
    font-family: 'Roboto Slab', serif;
    
}
img {
  height: 500px;
  width: auto;
  margin: 0 auto;
  display:block;
}
h1 {
    font-size: 45px;
    letter-spacing: 0.05em;
    font-weight: 400;
}
h4 {
    text-align: justify;
    font-size: 16px;
    font-weight: 500;
}
.tips {
    font-family: 'Indie Flower', cursive;
}
.name {
    text-align: right;
    font-size: 10px;
}
h5 {
    color: #ffa320;
}
.list_wrap{
    background-color: #cdcbbb ;
}
.list_box{
    border: 0.1px solid #382611;
    color: #e29922;
    text-transform: uppercase;
}
img:hover {
    transform: scale(1.2);
    transition: 2s;
}

</style>



