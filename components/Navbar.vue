<template>
  <div>
    <UColorModeButton />
    <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark px-0 py-3 navbar-bordered">
      <div class="container-xl">
        <!-- Logo -->
        <NuxtLink to="/">
          <!-- <img src="/assets/topupin-logo.png" class="logo" alt="..." /> -->
        </NuxtLink>
        <!-- Navbar toggle -->
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarCollapse"
          aria-controls="navbarCollapse"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <!-- Collapse -->
        <div class="collapse navbar-collapse" id="navbarCollapse">
          <!-- Nav -->
          <div class="navbar-nav mx-lg-auto">
            <NuxtLink
              to="/"
              class="nav-item anim-border-bottom nav-link"
              aria-current="page"
            >Home</NuxtLink>
  
            <NuxtLink
              to="/Projects"
              class="nav-item anim-border-bottom nav-link"
              aria-current="page"
            >Projects</NuxtLink>
  
            <NuxtLink
              to="/About"
              class="nav-item anim-border-bottom nav-link"
              aria-current="page"
            >About</NuxtLink>
  
            <NuxtLink
              to="/Contact"
              class="nav-item anim-border-bottom nav-link"
              aria-current="page"
            >Contact</NuxtLink>
          </div>
          <!-- Right navigation -->
        </div>
      </div>
    </nav>
  </div>
  </template>
  <!--  -->
  <script>
  export default {
    name: 'Navbar'
  };
  </script>
  
  <style scoped>
  .navbar-dark.bg-dark {
    background-color: #0f172a !important;
  }
  
  .navbar-bordered {
    border-bottom: 2px solid #01c879 ;
  }
  
  .logo {
    width: 100px;
    margin: 0;
    padding: 0;
  }
  
  @media only screen and (max-width: 500px) {
    .logo {
      width: 90px;
    }
  }
  
  .nav-link {
    font-weight: 600;
    margin-right: 20px;
    position: relative;
    padding-bottom: 4px;
    transition: color 0.2s ease-out;
  }
  
  .anim-border-bottom {
    position: relative;
    overflow: hidden;
  }
  
  .anim-border-bottom::after {
    content: "";
    position: absolute;
    width: 100%;
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #01c879;
    transform: scaleX(0);
    transform-origin: bottom left;
    transition: transform 0.2s ease-out;
  }
  
  .anim-border-bottom:hover::after {
    transform: scaleX(1);
  }
  
  .active.nav-item {
    border-bottom: 2px #01c879 solid;
  }
  </style>
  