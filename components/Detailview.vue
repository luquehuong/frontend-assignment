<template>
    <div class="detail_bar p-10 flex flex-wrap">
        <div class="img_bar w-1/3">
            <img :src="beer_show.image_url" class="ml-auto">
        </div>
        <div class="info_bar w-2/3 pt-10">
            <h1 class="text-center">{{beer_show.name}}</h1>
            <h5 class="text-center pb-10">{{beer_show.tagline}}</h5>
            <h4 class="pb-3">{{beer_show.description}}</h4>
            <ul class="pb-10">
                <li v-for="item in beer_show.food_pairing" :key="item">{{item}}</li>
            </ul>
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
img {
  height: 500px;
  width: auto;
  margin: 0 auto;
  display:block;
}
h1 {
    font-size: 45px;
    letter-spacing: 0.05em;
}
h4 {
    text-align: justify;
}
.tips {
    font-family: 'Indie Flower', cursive;
}
.name {
    text-align: right;
    font-size: 10px;
}
</style>



