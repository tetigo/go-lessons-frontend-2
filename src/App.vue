<template>
  <NavBar />
  <div class="container">
    <div class="row">
      <div class="col-12 d-flex justify-content-center">
        <CarouselItem />
      </div>
    </div>
    <div class="row">
      <div class="col-md-2 col-6 d-flex justify-content-center">
        text1
      </div>
      <div class="col-md-8 col-6 d-flex justify-content-center">
        text2
      </div>
      <div class="col-md-2 col-12 d-flex justify-content-center">
        text3
      </div>
    </div>
  </div>
</template>

<script>
import CarouselItem from './components/CarouselItem.vue'
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    CarouselItem,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
