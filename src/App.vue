<script setup>
import './style.css'
import Header from './components/Header.vue'
import Menu from './components/Menu.vue'
import ProfileCard from './components/ProfileCard.vue'
import Buttons from './components/Buttons.vue'
import Carousel from './components/Carousel.vue'
import Article from './components/Article.vue'
import Footer from './components/Footer.vue'
import PokeApi from './components/PokeApi.vue'

</script>

<template>
  <div class="app">
    <Header />
    <Menu />
    <ProfileCard />
    <Buttons />
    <PokeApi />
    <Carousel />      
    <Article />
    <Footer />    
  </div>
</template>


