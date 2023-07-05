<template>
  <NavBar />
  <div class="container">
    <div class="row">
      <div class="col-12 d-flex justify-content-center">
        <CarouselItem />
      </div>
    </div>
    <h3 class="mt-3">Popular Products</h3>
    <div class="row">
      <div class="col-12 col-md-3 d-flex justify-content-center mt-3">
        <ProductThumb
          price="12 EUR"
          title="Product Name1"
          additionalInfo="New"
        />
      </div>
      <div class="col-12 col-md-3 d-flex justify-content-center mt-3">
        <ProductThumb
          price="15 EUR"
          title="Product Name2"
          additionalInfo="New"
        />
      </div>
      <div class="col-12 col-md-3 d-flex justify-content-center mt-3">
        <ProductThumb
          price="17 EUR"
          title="Product Name3"
          additionalInfo="New"
        />
      </div>
      <div class="col-12 col-md-3 d-flex justify-content-center mt-3">
        <ProductThumb
          price="11 EUR"
          title="Product Name4"
          additionalInfo="New"
        />
      </div>
    </div>
  </div>
</template>

<script>
import CarouselItem from './components/CarouselItem.vue'
import NavBar from './components/NavBar.vue'
import ProductThumb from './components/ProductThumb.vue'
import WebServices from './webservices'

export default {
  name: 'App',
  components: {
    NavBar,
    CarouselItem,
    ProductThumb,
  },
  created() {
    WebServices.getProducts()
      .then((res) => {
        alert(res.data)
      })
      .catch((err) => {
        alert(err)
      })
    WebServices.getCategories()
      .then((res) => {
        alert(res.data)
      })
      .catch((err) => {
        alert(err)
      })
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
