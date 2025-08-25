<template>
  <nav class="navbar" :class="{ scrolled: isScrolled }">
    <div class="nav-container">
      <div class="nav-logo">
        <a href="#" class="logo-link">joeljacob.</a>
      </div>
      <ul class="nav-menu">
        <li class="nav-item">
          <a href="#" class="nav-link">Home</a>
        </li>
        <li class="nav-item">
          <a href="#about" class="nav-link">About</a>
        </li>
        <li class="nav-item">
          <a href="#works" class="nav-link">Works</a>
        </li>
        <li class="nav-item">
          <a href="#contact" class="nav-link">Contact</a>
        </li>
      </ul>
      <div class="hire-me-btn">
        <a href="#contact" class="hire-btn">
          Hire Me
          <svg
            class="arrow"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            fill="none"
          >
            <path
              d="M17 7L6 18"
              stroke="currentColor"
              stroke-width="1.5"
              stroke-linecap="round"
            ></path>
            <path
              d="M11 6.13151C11 6.13151 16.6335 5.65662 17.4885 6.51153C18.3434 7.36645 17.8684 13 17.8684 13"
              stroke="currentColor"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
          </svg>
        </a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavigationBar',
  data() {
    return {
      isScrolled: false,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 50
    },
  },
}
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background: transparent;
  backdrop-filter: none;
  z-index: 1000;
  padding: 1rem 0;
  transition: all 0.3s ease;
  font-family: 'Gilroy-Medium', 'Gilroy', sans-serif;
  font-weight: 500;
}

.navbar.scrolled {
  background: #000000;
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
}

.nav-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-link {
  font-size: 32px;
  font-family: 'Gilroy-Medium', 'Gilroy', sans-serif;
  font-weight: 500;
  color: #e7e7e7;
  text-decoration: none;
  transition: color 0.3s ease;
}

.navbar.scrolled .logo-link {
  color: #e7e7e7;
}

/* .logo-link:hover {
  color: #00ffa5;
} */

.nav-menu {
  display: flex;
  list-style: none;
  gap: 2.5rem;
}

.nav-link {
  color: #e7e7e7;
  text-decoration: none;
  font-family: 'Gilroy-Medium', 'Gilroy', sans-serif;
  font-weight: 500;
  font-size: 16px;
  transition: color 0.3s ease;
  position: relative;
}

.navbar.scrolled .nav-link {
  color: #e7e7e7;
}

/* .nav-link:hover {
  color: #00ffa5;
} */

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: #00ffa5;
  transition: width 0.3s ease;
}

/* .nav-link:hover::after {
  width: 100%;
} */

.hire-btn {
  background: #e7e7e7;
  color: black;
  padding: 0.75rem 1.5rem;
  border-radius: 0;
  text-decoration: none;
  font-family: 'Gilroy-Medium', 'Gilroy', sans-serif;
  font-weight: 500;
  font-size: 16px;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  transition: all 0.3s ease;
}

.navbar.scrolled .hire-btn {
  background: #e7e7e7;
  color: #000000;
}

/* .hire-btn:hover {
  background: #00ffa5;
  color: black;
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(100, 255, 218, 0.3);
} */

.arrow {
  transition: transform 0.3s ease;
}

.hire-btn:hover .arrow {
  transform: translateX(3px);
}

@media (max-width: 768px) {
  .nav-menu {
    display: none;
  }

  .nav-container {
    padding: 0 1rem;
  }

  .logo-link {
    font-size: 28px;
  }

  .hire-btn {
    font-size: 14px;
    padding: 0.6rem 1.2rem;
  }
}
</style>
