<template>
  <div
    id="carouselExampleControls"
    class="carousel slide carousel-custom"
    data-bs-ride="carousel"
  >
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img
          src="@/assets/botties.jpg"
          class="d-block w-100"
          alt="little booties"
        />
      </div>
      <div class="carousel-item">
        <img
          src="@/assets/fashion.jpg"
          class="d-block w-100"
          alt="fashion blouse"
        />
      </div>
      <div class="carousel-item">
        <img src="@/assets/scarpin.jpg" class="d-block w-100" alt="scarpin" />
      </div>
    </div>
    <button
      class="carousel-control-prev"
      type="button"
      data-bs-target="#carouselExampleControls"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button
      class="carousel-control-next"
      type="button"
      data-bs-target="#carouselExampleControls"
      data-bs-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'CarouselItem',
}
</script>

<style scoped>
.carousel-custom {
  max-width: 600px;
}
</style>
