<template>
  <div>
    <HeaderTest/>
    <BannerTest/>
    <span class="span">Assista a seguir</span>
    <MoreMovies/>
    <br>
    <br>
    <span class="span2">Mais assistidos</span>
    <MoviesTest/>

  </div>
</template>

<script>
import HeaderTest from '../src/components/HeaderTest.vue'
import BannerTest from '../src/components/BannerTest.vue'
import MoreMovies from '../src/components/MoreMovies.vue'
import MoviesTest from '../src/components/MoviesTest.vue'
import '@fortawesome/fontawesome-free/css/all.css'
export default {
    name: 'App',
    components: { HeaderTest, BannerTest, MoreMovies, MoviesTest }
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

  .span, 
  .span2{
    color: #fff;
    font-weight: bold;
    margin-left: 105px;
  }
</style>
