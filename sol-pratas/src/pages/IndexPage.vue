<template>
<q-page class="row bg-yellow-1">
  <div class="w100  row justify-center">
    <q-carousel
    animated
    v-model="slide"
    navigation
    infinite
    :autoplay="autoplay"
    arrows
    transition-prev="slide-right"
    transition-next="slide-left"
    @mouseenter="autoplay = false"
    @mouseleave="autoplay = true"
  >
    <q-carousel-slide :name="1" img-src="https://lojavivara.vtexassets.com/unsafe/fit-in/1920x720/center/middle/https%3A%2F%2Flojavivara.vtexassets.com%2Fassets%2Fvtex.file-manager-graphql%2Fimages%2F0df2530c-611e-42c2-91e7-d714fe3262e7___efb353dfc4f9c9e156ac266847cbb671.png" />
    <q-carousel-slide :name="2" img-src="https://global.cdn.magazord.com.br/glamourpratas/img/2023/08/banner/2928/banner-site-mais-vendidos-desktop-1980-550-px.png" />
    <q-carousel-slide :name="3" img-src="https://cdn.spiritshop.com.br/lumae/image/data/lumae-v2/banner/home/2022/10-outubro/bn-pagamento-a-vista.jpg" />
  </q-carousel>
  <DestaquesComponent />
  <div class="w100 footer q-pt-xl q-pb-md footer column justify-center">
    <div class="row justify-center q-gutter-x-md items-center">
      <a class="insta" href="https://www.instagram.com/solpratas_val/" target="_blank">Nosso Instagram</a>
      <q-icon name="add_a_photo" color="grey-8" size="md"/>
    </div>
    <div class="row justify-center q-gutter-x-md items-center">
      <a class="text-blue-5 text-weight-bold q-mt-md" target="_blank" href="https://samuelvictorol.github.io/portfolio/home">Powered by: Samuel Victor</a>
    </div>
  </div>
</div>
</q-page>
</template>

<script setup lang="ts">
import DestaquesComponent from '../components/DestaquesComponent.vue'
import { ref } from 'vue'

const slide = ref(1)
const autoplay = ref(true)

</script>
<style scoped>
.q-page {
height: 110vh;
}

.q-carousel {
  width: 100%;
}

.footer {
  background: #fffc00;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #FFFDE7, #f6f493);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #FFFDE7, #f6f493); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
.insta{
  text-decoration: none;
  color: black;
  font-family: 'Satisfy', sans-serif;
  font-size: 2rem;
  opacity: 0.8;
}

a{
  opacity: 0.8;
}

a:hover {
  opacity: 1;
  color: rgb(32, 102, 137);
  transition: all 0.3s linear
}

@media (max-width:1200px) {
  .q-carousel {
    height: 20vh;
    margin-bottom: 1rem;
  }
}
</style>
