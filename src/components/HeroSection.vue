<template>
  <section class="hero">

    <div class="gradient-decoration gradient-top-left"></div>
    <div class="gradient-decoration gradient-top-right"></div>
    
    <div class="hero-container">
      <div class="hero-content">
        <!-- Center: UI/UX & GRAPHIC -->
        <div class="center-title">
          <h1 class="main-title">
            <span>UI/UX &</span>
            <span style="margin-left: 10rem;">GRAPHIC</span>
          </h1>
        </div>

        <!-- Profile Image - Now at bottom -->
        <div class="profile-image">
          <img src="../assets/images/profile.png" alt="Joel Jacob Thomas" class="profile-img" />
        </div>

        <!-- Bottom Center: DESIGNER -->
        <div class="bottom-title">
          <h2 class="designer-title">DESIGNER</h2>
        </div>

        <!-- Left Content -->
        <div class="left-content">
          <p class="hero-name">JOEL JACOB THOMAS</p>
          <span class="left-label">DEFINING<br />DIGITAL ELEGANCE</span>
        </div>

        <!-- Right Content -->
        <div class="right-content">
          <p class="hero-description">
            I'm committed to designing interfaces <br> visuals that connect people to <br> ideas, turning
            complex visions into <br> elegant, impactful realities.
          </p>
          <span class="right-label">DESIGN<br />WITHOUT COMPROMISE</span>
        </div>

        <!-- Gradient Decorative Elements -->
       <div class="gradient-decoration gradient-bottom-right"></div>
       <div class="gradient-decoration gradient-bottom-left"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Khand:wght@600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Gilroy:wght@500&display=swap');

.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 4rem 0;
  position: relative;
  background: #000;
  color: #E7E7E7;
  overflow: hidden;
}

/* Gradient Decorative Elements */
.gradient-decoration {
  position: absolute;
  pointer-events: none;
  /* z-index: 0; */
  opacity: 0.2;
  filter: blur(100px);
}

.gradient-top-right {
  top: -5%;
  right: -10%;
  width: 60%;
  height: 50%;
  background: linear-gradient(#0F0061 0%, #0F0061 100%);
  border-radius: 100%;
}

.gradient-bottom-left {
  bottom: -40%;
  left: -40%;
  width: 100%;
  height: 100%;
  background: linear-gradient(#0F0061 0%, #0F0061 100%);
  border-radius: 100%;
  z-index: 6;
}

.gradient-bottom-right {
  bottom: -40%;
  right: -40%;
  width: 100%;
  height: 100%;
  background: linear-gradient(#005537 0%, #005537 100%);
  border-radius: 100%;
  z-index: 6;
}

.gradient-top-left {
  top: -8%;
  left: -10%;
  width: 50%;
  height: 60%;
  background: linear-gradient(#005537 0%, #005537 100%);
  border-radius: 100%;
}

.hero-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  width: 100%;
  position: relative;
  z-index: 1;
}

.hero-content {
  position: relative;
  width: 100%;
  height: 80vh;
  display: grid;
  place-items: center;
}

/* Center Title - UI/UX & GRAPHIC */
.center-title {
  position: absolute;
  top: 15%;
  left: 50%;
  transform: translateX(-50%);
  z-index: 1;
}

.main-title {
  font-family: 'Khand', sans-serif;
  font-weight: 600;
  font-size: 200px;
  line-height: 0.8;
  text-transform: uppercase;
  letter-spacing: -0.02em;
  margin: 0;
  text-align: center;
  white-space: nowrap;
  color: #E7E7E7;
}

/* Profile Image - Moved to bottom */
.profile-image {
  position: absolute;
  bottom: -12%;
  left: 50%;
  transform: translateX(-50%);
  width: 775px;
  height: 875px;
  overflow: hidden;
  z-index: 5;
}

.profile-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: grayscale(100%) contrast(110%) brightness(110%);
  transition: filter 0.3s ease;
}

/* Bottom Title - DESIGNER - Most front */
.bottom-title {
  position: absolute;
  bottom: -2%;
  left: 50%;
  transform: translateX(-50%);
  z-index: 200;
}

.designer-title {
  font-family: 'Khand', sans-serif;
  font-weight: 600;
  font-size: 200px;
  line-height: 0.8;
  text-transform: uppercase;
  letter-spacing: -0.02em;
  margin: 0;
  text-align: center;
  background: #E7E7E7;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  white-space: nowrap;
}

/* Left Content - Most front */
.left-content {
  position: absolute;
  top: 68.5%;
  left: 6%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 18.5rem;
  z-index: 200;
}

.hero-name {
  font-family: 'Gilroy', sans-serif;
  font-weight: 500;
  font-size: 1.1rem;
  letter-spacing: 0.1em;
  color: #E7E7E7;
  margin: 0;
}

.left-label {
  font-family: 'Gilroy', sans-serif;
  font-weight: 500;
  font-size: 0.85rem;
  line-height: 1.4;
  color: #E7E7E7;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

/* Right Content - Most front */
.right-content {
  position: absolute;
  top: 66%;
  right: 6%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 15rem;
  max-width: 350px;
  z-index: 200;
  text-align: left;
  align-items: flex-end;
}

.hero-description {
  font-family: 'Gilroy', sans-serif;
  font-weight: 500;
  font-size: 1rem;
  line-height: 1.6;
  color: #E7E7E7;
  margin: 0;
  text-align: left;
}

.right-label {
  font-family: 'Gilroy', sans-serif;
  font-weight: 500;
  font-size: 0.85rem;
  line-height: 1.4;
  color: #E7E7E7;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  text-align: left;
}

/* Responsive Design */
@media (max-width: 1200px) {
  .main-title,
  .designer-title {
    font-size: 150px;
  }

  .left-content {
    left: 3%;
  }

  .right-content {
    right: 3%;
    max-width: 300px;
  }

  .profile-image {
    width: 350px;
    height: 450px;
  }
}

@media (max-width: 968px) {
  .main-title,
  .designer-title {
    font-size: 100px;
  }

  .profile-image {
    width: 300px;
    height: 380px;
    bottom: -5%;
  }

  .bottom-title {
    bottom: 30%;
  }

  .left-content,
  .right-content {
    position: static;
    transform: none;
    max-width: 100%;
    text-align: center;
    align-items: center;
  }

  .hero-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    height: auto;
    min-height: 80vh;
  }

  .center-title,
  .bottom-title {
    position: static;
    transform: none;
  }

  .profile-image {
    position: static;
    transform: none;
    order: 3;
  }

  .hero-description,
  .right-label {
    text-align: center;
  }
}

@media (max-width: 640px) {
  .hero {
    padding: 2rem 0;
  }

  .hero-container {
    padding: 0 1rem;
  }

  .main-title,
  .designer-title {
    font-size: 60px;
  }

  .profile-image {
    width: 250px;
    height: 320px;
  }

  .right-content {
    max-width: 280px;
  }
}
</style>