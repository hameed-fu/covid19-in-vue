<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <router-link class="navbar-brand" to="/">Navbar</router-link>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <router-link  class="nav-link" to="/"
              >Home <span class="sr-only"></span></router-link 
            >
          </li>
          <!-- <li class="nav-item">
            <router-link  class="nav-link" to="about">About Us</router-link>
          </li>
          <li class="nav-item">
            <router-link  class="nav-link" to="contact">Contact</router-link>
          </li> -->
          <li class="nav-item">
            <router-link  class="nav-link" to="covid">Covid Latest data</router-link>
          </li>
          <li class="nav-item">
            <router-link  class="nav-link" to="products">Products</router-link>
          </li>
          <!-- <li class="nav-item">
            <router-link  class="nav-link" to="login">Login</router-link>
          </li> -->
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
    // name:'NavBar'
};
</script>

<style>
</style>