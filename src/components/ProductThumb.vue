<template>
  <div class="card" style="width: 12rem;">
    <img src="@/assets/botties.jpg" class="card-img-top" alt="little booties" />
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p class="card-text">
        {{ price }}
      </p>
      <p class="card-text">
        {{ additionalInfo }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductThumb',
  props: {
    title: String,
    price: String,
    additionalInfo: String,
  },
}
</script>

<style scoped></style>
