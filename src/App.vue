<template>
  <div>
    <HeaderTest/>
    <BannerTest/>
    <div class="span">Assista a seguir</div>
    <MoreMovies :banners="banners1"/>
    <div class="span">Mais assistidos</div>
    <MoreMovies :banners="banners2"/>

  </div>
</template>

<script>
import HeaderTest from '../src/components/HeaderTest.vue'
import BannerTest from '../src/components/BannerTest.vue'
import MoreMovies from '../src/components/MoreMovies.vue'

import '@fortawesome/fontawesome-free/css/all.css'

const banners1 = [
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


const banners2 = [
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
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/2f4f4632e0873ff79035ec26bcee8605049d4d5261524f30b724904f58cba6ae._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 8,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/59898e3b729756b7e12e43f511ffa9c4446745890d644e96d630cc85a7c49f4f._UY500_UX667_RI_V_TTW_.jpg'
    }
]

export default {
    name: 'App',
    data(){
      return{
        banners1,
        banners2
      }
    },
    components: { HeaderTest, BannerTest, MoreMovies }
}
</script>

<style>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
    background-color: #0f171e;
  }

  .span{
    color: #fff;
    font-size:11px;
    font-weight: bold;
    padding: 0 7%;
    margin-bottom: 5px;
  }
</style>
