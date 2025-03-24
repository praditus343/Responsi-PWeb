<template>
  <div>
    <UColorModeButton />
    <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark px-0 py-3 navbar-bordered">
      <div class="container-xl">
        <!-- Logo -->
        <NuxtLink to="/" class="navbar-brand">
          <!-- <img src="/assets/topupin-logo.png" class="logo" alt="Logo" /> -->
        </NuxtLink>
        
        <!-- Navbar toggle -->
        <button
          class="navbar-toggler custom-toggler"
          type="button"
          @click="toggleMenu"
          aria-controls="navbarCollapse"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        
        <!-- Collapse -->
        <div 
          class="collapse navbar-collapse" 
          :class="{ 'show': isMenuOpen }" 
          id="navbarCollapse"
        >
          <!-- Nav -->
          <div class="navbar-nav mx-lg-auto">
            <NuxtLink
              to="/"
              class="nav-item nav-link anim-border-bottom"
              active-class="active"
              exact
              @click="closeMenu"
            >Home</NuxtLink>
  
            <NuxtLink
              to="/Projects"
              class="nav-item nav-link anim-border-bottom"
              active-class="active"
              @click="closeMenu"
            >Projects</NuxtLink>
  
            <NuxtLink
              to="/Contact"
              class="nav-item nav-link anim-border-bottom"
              active-class="active"
              @click="closeMenu"
            >Contact</NuxtLink>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    },
    closeMenu() {
      this.isMenuOpen = false
    }
  },
  mounted() {
    // Close menu when clicking outside
    document.addEventListener('click', (e) => {
      const navbar = document.getElementById('navbarCollapse')
      const toggler = document.querySelector('.navbar-toggler')
      if (this.isMenuOpen && navbar && !navbar.contains(e.target) && !toggler.contains(e.target)) {
        this.isMenuOpen = false
      }
    })
  },
  beforeDestroy() {
    // Clean up event listener
    document.removeEventListener('click', this.closeMenu)
  }
}
</script>

<style scoped>
.navbar-dark.bg-dark {
  background-color: #0f172a !important;
}

.navbar-bordered {
  border-bottom: 2px solid #01c879;
}

.logo {
  width: 100px;
  height: auto;
  margin: 0;
  padding: 0;
}

.nav-link {
  font-weight: 600;
  margin-right: 20px;
  position: relative;
  padding: 0.5rem 1rem;
  color: rgba(255, 255, 255, 0.85) !important;
  transition: color 0.2s ease-out, transform 0.2s ease-out; /* Added transform to transition */
}

.nav-link:hover {
  color: #ffffff !important;
  transform: scale(1.05); /* Slight scale effect on hover */
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

/* Active state */
.active {
  border-bottom: 2px solid #01c879;
  transition: border-bottom-color 0.2s ease-out; /* Smooth transition for active state */
}

/* Custom toggler styling */
.custom-toggler {
  border: 1px solid #01c879 !important;
  padding: 0.25rem 0.5rem;
  transition: background-color 0.2s ease-out; /* Smooth background color transition */
}

.custom-toggler:hover {
  background-color: rgba(1, 200, 121, 0.1); /* Background on hover */
}

/* Mobile Styles */
@media (max-width: 991.98px) {
  .navbar-collapse {
    background-color: #0f172a;
    padding: 1rem;
    margin: 0 -1rem;
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    z-index: 1000;
    transition: height 0.3s ease-in-out;
  }

  .navbar-collapse.show {
    display: block !important;
  }

  .navbar-nav {
    padding: 0.5rem 0;
  }

  .nav-item {
    margin: 0.5rem 0;
    text-align: center;
  }

  .nav-link {
    margin-right: 0;
    padding: 0.75rem 1rem;
    display: block;
    width: 100%;
  }

  .logo {
    width: 90px;
  }
}

/* Small mobile devices */
@media (max-width: 767px) {
  .navbar-dark .navbar-nav .nav-link {
    font-size: 16px;
  }

  .container-xl {
    padding-left: 1rem;
    padding-right: 1rem;
  }
}
</style>