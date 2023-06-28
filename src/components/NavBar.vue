<template>
  <nav class="navbar navbar-light bg-light fixed-top navbar-expand-lg">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img
          src="@/assets/gopher-favicon.png"
          alt=""
          width="30"
          height="24"
          class="d-inline-block align-text-top"
        />
        Gopher E-commerce
      </a>
      <!-- dropdown button -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <!-- links -->
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">Plushes</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Clothes</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Acessories</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">
              <UserIcon />
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">
              <CartIcon />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import UserIcon from './icons/UserIcon.vue'
import CartIcon from './icons/CartIcon.vue'
export default {
  name: 'NavBar',
  components: {
    UserIcon,
    CartIcon,
  },
}
</script>

<style scoped></style>
