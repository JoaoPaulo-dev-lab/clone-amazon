<template>
  <div>
    <HeaderTest/>
    <BannerTest/>
    <div class="span">Assista a seguir</div>
    <MoreMovies :banners="banners1"/>
    <div class="span">Mais assistidos</div>
    <MoreMovies :banners="banners2"/>
    <div class="span">Filmes recomendados</div>
    <MoreMovies :banners="banners3"/>
    <div class="span">Melhores filmes</div>
    <MoreMovies :banners="banners4"/>
    <div class="span">Filmes de comédia</div>
    <MoreMovies :banners="banners5"/>
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
const banners3 = [
    {
        id: 1,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/e85435452c687826f4898a4e790ca563a0be960ff4d7e2b557e8f032f49e15a7._UY500_UX667_RI_V_TTW_.png'
    },
    {
        id: 2,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/adb49794a3877207783f1fbccad15964bdf4209c1f72b7f758f12ddd74f24c33._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 3,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/e6455a8504e4292716f8ad0d2c02e04509dd6e86be55cc1125df9b877bb89f04._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 4,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/6c122a28cbcb4f3433f4bc47dd3041a3234a8774d0c999f0641080a2fda9d059._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 5,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/a02eab0a2ffd89593dc621c66b531dd59980c89fd81033bc61674429043426aa._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 6,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/1cad8b21e10a068bd9dfa9e16503fae899e53d037557697a7bf0b910aa012820._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 7,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/17de976aa3eef0ae588a0cfcfd920aa35a0541e5c41d27d30485e21d0c89fba8._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 8,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/f57469e0cb35f51aef483e2c5aa00ca8ed0b33363012eca2656dcb67c2b98eea._UY500_UX667_RI_V_TTW_.jpg'
    }
]
const banners4 = [
    {
        id: 1,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/fbd9262f76f6feb91d05abea759f58644eb54f4ef8ff1a07e64a7908c8620eb0._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 2,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/569abce1202d4157423e384bd7a5fb1efce2c8399bf6125703edc708e56d2ec6._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 3,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/7627b4bc590d30635ab63835635282e4ff8a98d52c9c7b76a93cd2e79336db5c._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 4,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/11c72dd35223e9a4f5e460f975e4a10fbc469da53a08c4830a3e99d33b457bb8._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 5,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/8e791dfabd3deb6241cf667ba1b8f57bda1d8a5a36a1e22cc0dcf41a28205eb2._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 6,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/8cc15cef464265a8ea09d0cfe85ce375ca1e6cc5f93fe8e679ccd8169e9ba75b._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 7,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/699e933942eda51a1883b31e51496b898d3475d972f25cdb2d36f3fbb8642500._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 8,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/079300a17c59a1b73d2f1efbfe87438eca3e42b18fa89deacb24a123b5aae9a0._UY500_UX667_RI_V_TTW_.jpg'
    }
]
const banners5 = [
    {
        id: 1,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/9d4b5caf650861be0ba1a8cecb4bf32c2daf3856b86b6979a9bbe36cec0b5e3d._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 2,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/b9d7db5a177438cfd8b82ad39a0faeae2e36b81427992290e43f27d83a48718c._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 3,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/a7b76ec9e674a82a41cfdf1fccc2011ed6b6149ee3943fa664a896090cac5054._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 4,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/be5140cf94089854654828b4174608aa30b95c23dbd03293df54eb60c4b94f82._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 5,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/02622f1559c2e654718e4c7736731536d20215f3c77ec1b2dfc9a494aea2f69a._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 6,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/69af9f1f61fa4338b2a038b8ab0fef8f91ec6272ace09f8571edc03779680c37._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 7,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/e81379689d8ada79a7d9eb5ed54cfc3bb20325464f5e0362f47122a19ec9209a._UY500_UX667_RI_V_TTW_.jpg'
    },
    {
        id: 8,
        bannerURL: 'https://images-na.ssl-images-amazon.com/images/S/pv-target-images/7aef0e85be40b55a6a16bdee18917efaa640bdacf4b74d7abb7f90b125c65cb7._UY500_UX667_RI_V_TTW_.jpg'
    }
]

export default {
    name: 'App',
    data(){
      return{
        banners1,
        banners2,
        banners3,
        banners4,
        banners5
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
  }

    body{
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
