<template>
        <div class="container-slider2">
            <carousel   :items-to-show="numberSliders || 4">
                <slide   v-for="banner in banners" :key="banner.id">
                    <div :style="{'background-image': `url(${banner.bannerURL})`}" class="banner2"></div>
                </slide>
                <template #addons>
                    <div >
                   
                    </div>
                </template>
            </carousel>
            <div class="gradient2 left"></div>
            <div class="gradient2 right"></div>
        </div>
</template>

<script>
// carousel__prev carousel__prev--in-active
// carousel__icon
import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide} from 'vue3-carousel'
export default {
    name: 'MoreMovies',
    components: {Carousel, Slide },
    props:{
        banners: Array
    },
    data() {
        return {
            numberSliders:4
        }
    },
    methods:{
        setNumbersSliders(){
            const width = window?.innerWidth

            if(width >= 1100)
            this.numberSliders = 4
            else if(width > 400 && width < 1100)
            this.numberSliders = 3
            else if(width <= 400)
            this.numberSliders = 2
        }
    },
    mounted(){
        this.setNumbersSliders()
        window?.addEventListener('resize', this.setNumbersSliders)
    },   
}
</script>

<style scoped>
    .container-slider2{
        width: 100%; 
        padding: 0 5%;
        position: relative;
        margin: 10px 0 30px 0;
    }
    .gradient2{
        position: absolute;
        width: 7%;
        height: 200px;
        background-color: #0f171e;
        top: 0;
        z-index: 0;
    }

    .right {
        right: 0;
    }

    .left{
        left: 0;
    }

    .banner2{
        width: 400px; 
        height: 200px;
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        border: 10px solid rgba(0, 0, 0, 0);
        transition: 1s;
        cursor: pointer;
    }

    .banner2:hover{
        transform: scale(1.1, 1.1);
    }

    .carousel__prev,.carousel__next{z-index: 99999;background-color: #0e88b1;}

    .carousel__icon{background-color:#0e88b1;border-radius: 50%;}

    @media screen and (max-width: 1465px) {
    .gradient2{
        position: absolute;
        width: 7%;
        height: 150px;
        background-color: #0f171e;
        top: 0;
        z-index: 0;
    }

    .banner2{
        width:350px; 
        height: 150px;
        border: 10px solid rgba(0, 0, 0, 0);
    }
    }

    @media screen and (max-width: 1070px) {
    .banner2{
        margin-right: 10px;
    }
    }

    @media screen and (max-width: 950px) {
    .gradient2{
        position: absolute;
        width: 7%;
        height: 130px;
        background-color: #0f171e;
        top: 0;
        z-index: 0;
    }
    .banner2{
        width:300px; 
        height: 130px;
        border: 0px solid rgba(0, 0, 0, 0);
    }
    }

    @media screen and (max-width: 750px) {
    .gradient2{
        position: absolute;
        width: 7%;
        height: 100px;
        background-color: #0f171e;
        top: 0;
        z-index: 0;
    }
    .banner2{
        width:300px !important; 
        height: 100px;
        border: 0px solid rgba(0, 0, 0, 0);
    }
    }
</style>