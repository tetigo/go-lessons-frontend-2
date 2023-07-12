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
      <div
        v-for="product in products"
        :key="product.id"
        class="col-12 col-md-3 d-flex justify-content-center mt-3"
      >
        <ProductThumb
          :title="product.name"
          :price="product.totalPrice.display"
          :additionalInfo="product.shortDescription"
          :imageUrl="product.image"
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
  data() {
    return {
      products: null,
      categories: null,
    }
  },
  created() {
    WebServices.getProducts()
      .then((res) => {
        this.products = res.data
      })
      .catch((err) => {
        console.log(err)
      })
    WebServices.getCategories()
      .then((res) => {
        this.categories = res.data
      })
      .catch((err) => {
        console.log(err)
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
