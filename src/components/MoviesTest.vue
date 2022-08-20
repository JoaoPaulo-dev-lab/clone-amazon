<template>
    <div class="container-slider3">
            
            <carousel   :items-to-show="4">
                <slide   v-for="banner in banners" :key="banner.id">
                    <div :style="{'background-image': `url(${banner.bannerURL})`}" class="banner3">

                    </div>
                </slide>

                <template #addons>
                    <div >
                   
                    </div>
                </template>
            </carousel>
            <div class="gradient3 left"></div>
            <div class="gradient3 right"></div>
        </div>
</template>

<script>

const banners = [
    {
        id: 1,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/06f12defae29da5fb93c184e0573af237b93df8d6a6d2e8dc9a9b5c0d4c3e951._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 2,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/7e5e00e5bb4d0f724811ea3817c312ceaaae14f4a52636e65fd8bca82be98943._UY500_UX667_RI_V_TTW_.png'
    },
    {
        id: 3,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/a92d9fecc2c1bdeda42b9dcdd43b69568fad3ef4a65cc7b730e9ade659a49edc._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 4,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/c026fcb0731f9e735e5df3a808afa15254a2c6ec2efb4e088f43a1767f41d8c9._RI_V_TTW_.jpg'
    },
    {
        id: 5,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/e4acfe046d5ddee75d55b6c5a77c6d3e4ef3b3c37b1946faa354a1697faba3f2._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 6,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/11c722a7ba6a7dfd600198b0593c739bc17b5daa9b3a615283623adbe1f32cbb._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 7,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/cde297dd4cf2e35c2261b0f3609b22461ee21afcb2f1c6af6a30b995e45d1956._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 8,
        bannerURL: 'https://images-eu.ssl-images-amazon.com/images/S/pv-target-images/d005998f8d2b18b0ed1a3c7b08c7ed9c4ecfd0dbae763a794bdf02391c7b28a5._UY500_UX667_RI_V_TTW_.jpg'
    }
]

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide } from 'vue3-carousel'

export default {
    name: 'MoviesTest',
    components: {Carousel, Slide},

    data() {
        return {banners}
    }
}
</script>

<style scoped>
    .container-slider3{
        width: 100%; 
        padding: 0 5%;
        position: relative;
        margin: 10px 0;
    }

    .gradient3{
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

    .banner3{
        width: 400px; 
        height: 200px;
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        border: 10px solid rgba(0, 0, 0, 0);
        transition: 1s;
        cursor: pointer;
    }

    .banner3:hover{
        transform: scale(1.1, 1.1);
    }

    .carousel__prev,.carousel__next{z-index: 99999;background-color: #0e88b1;}

    .carousel__icon{background-color:#0e88b1;border-radius: 50%;}

    
</style>