<template>
        <div class="container-slider">
            <carousel   :items-to-show="1">
            <slide   v-for="banner in banners" :key="banner.id">
                <div :style="{'background-image': `url(${banner.bannerURL})`}" class="banner"></div>
            </slide>
            <template #addons>
                <div >
                    <navigation  />
                </div>
            </template>
        </carousel>
            <div class="gradient left"></div>
            <div class="gradient right"></div>
        </div>
</template>

<script>
// carousel__prev carousel__prev--in-active
// carousel__icon

const banners = [
    {
        id: 1,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/5286a28e820e62b3a4b8d4fdb1f06f825c7e0a70b3e828da78244c013d04ddf1._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 2,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/64641e91f0851d0d3407913519a9c7d83e533f6aa756869c87abe59f1c93af4c._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 3,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/c3cd1188449a517cffc4ab3f6930df950f910ab09549e6205475cb4580c0b2da._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 4,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/c290144382e8410585ec86f839e0b4ecf3cc9be04d124dc2120254e0d8388d67._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 5,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/ec03c3557611683f2f19f679e63c61b9ce87b0fb9eaf823c665fa8356f442803._UY500_UX667_RI_V_TTW_.jpg'
    }
]

import 'vue3-carousel/dist/carousel.css';
import {Carousel, Navigation, Slide} from 'vue3-carousel'
export default {
    name: 'BannerTest',
    components: {Carousel, Navigation, Slide },

    data() {
        return {
            banners
        }
    }
}
</script>

<style>
    .container-slider{
        width: 100%; 
        padding: 0 5%;
        position: relative;
        margin: 10px 0 35px 0;
    }
    .gradient{
        position: absolute;
        width: 7%;
        height: 70vh;
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
    .banner{
        width: 100%;
        height: 70vh;
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;   
    }
    .carousel__prev,.carousel__next{z-index: 99999;background-color: #0e88b1;}
    .carousel__icon{background-color:#0e88b1;border-radius: 50%;}

    @media screen and (max-width:970px){
        .gradient{
        position: absolute;
        width: 7%;
        height: 45vh;
    }
        .banner{
        width: 100%;
        height: 45vh;
    }
    }

     @media screen and (max-width:500px){
        .gradient{
        position: absolute;
        width: 7%;
        height: 27vh;
        display: none;        
    }

    .carousel__prev,.carousel__next{display: none !important;}
    .carousel__icon{display:none;} 
       .banner{
        width: 100%;
        height: 27vh; 
    }
    }


    
</style>