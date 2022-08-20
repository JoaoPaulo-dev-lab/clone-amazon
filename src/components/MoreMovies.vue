<template>
    
        <div class="container-slider2">
            
            <carousel   :items-to-show="4">
                <slide   v-for="banner in banners" :key="banner.id">
                    <div :style="{'background-image': `url(${banner.bannerURL})`}" class="banner2">

                    </div>
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

const banners = [
    {
        id: 1,
        bannerURL: 'https://3.bp.blogspot.com/-RWEcd4H0wsU/V5C63x7PZYI/AAAAAAAAC9k/iCUbVt44kQUIs9wXu70e2uPAeQz-KaAvgCLcB/s1600/greys-anatomy-netflix-12-temporada.png'
    },
    {
        id: 2,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/da50c4cd9a1eb5e61085614b7bb55bae5a5a1a7b98b782193ac58c22736ebf5e._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 3,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/82ea5602114cd621aaae4847e68f1307a32ef0ac9637fbec637de284a2c5b4ec._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 4,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/9ba811446a506a577638cee9d1024c7900376c3aa1c4bea03d9648d200796385._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 5,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/0b11cbb26a03c5243711ea85605132eae458b68e4d6e98a16e22e230a2c406a6._V_SX1080_.jpg'
    },
    {
        id: 6,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/e5eb6f9efede6a6d972a76a091184d39b4e21a45d63525bf3b8cedcff3beb2c5._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 7,
        bannerURL: 'https://blog.livrariasfamiliacrista.com.br/wp-content/uploads/2019/07/At%C3%A9-o-ultimo-homem.jpg'
    },
    {
        id: 8,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/59898e3b729756b7e12e43f511ffa9c4446745890d644e96d630cc85a7c49f4f._UY500_UX667_RI_V_TTW_.jpg'
    }
]

import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide} from 'vue3-carousel'
export default {
    name: 'MoreMovies',
    components: {Carousel, Slide },

    data() {
        return {
            banners
        }
    }
}
</script>

<style scoped>
    .container-slider2{
        width: 100%; 
        padding: 0 5%;
        position: relative;
        margin: 10px 0;
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
        margin-left: 10px;
        transition: 1s;
        cursor: pointer;
    }

    .banner2:hover{
        transform: scale(1.1, 1.1);
    }

    .carousel__prev,.carousel__next{z-index: 99999;background-color: #0e88b1;}

    .carousel__icon{background-color:#0e88b1;border-radius: 50%;}

    
</style>