<template>
  <div id="app">
    <NavigationBar />
    <HeroSection />
    <AboutSection />
    <ContactSection />
  </div>
</template>

<script>
import NavigationBar from './components/NavigationBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ContactSection from './components/ContactSection.vue'

export default {
  name: 'App',
  components: {
    NavigationBar,
    HeroSection,
    AboutSection,
    ContactSection,
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Khand:wght@300;400;500;600;700&display=swap');

/* Gilroy TTF font face declarations */
@font-face {
  font-family: 'Gilroy';
  src: url('./assets/fonts/gilroy/Gilroy-Light.ttf') format('truetype');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Gilroy';
  src: url('./assets/fonts/gilroy/Gilroy-Regular.ttf') format('truetype');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Gilroy';
  src: url('./assets/fonts/gilroy/Gilroy-Medium.ttf') format('truetype');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Gilroy';
  src: url('./assets/fonts/gilroy/Gilroy-SemiBold.ttf') format('truetype');
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Gilroy';
  src: url('./assets/fonts/gilroy/Gilroy-Bold.ttf') format('truetype');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family:
    'Gilroy',
    'Khand',
    'Inter',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    'Roboto',
    sans-serif;
  background-color: #000000;
  color: white;
  overflow-x: hidden;
}

#app {
  min-height: 100vh;
}

/* Utility classes for specific font usage */
.font-gilroy {
  font-family: 'Gilroy', sans-serif;
}

.font-khand {
  font-family: 'Khand', sans-serif;
}
</style>
