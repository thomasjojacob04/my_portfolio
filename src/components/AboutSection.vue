<template>
  <section id="about" class="about">
    <div class="about-container">
      <div class="about-content">
        <div class="about-left">
          <h2 class="about-title">WHAT I DO</h2>
        </div>
        <div class="about-right">
          <p class="about-description">
            I craft visually striking, user-focused designs that blend creativity with strategy, from
            intuitive user interfaces and engaging user experiences to impactful branding, memorable
            logos, and compelling graphic designs. Every project I create is designed to tell a story,
            evoke emotion, and leave a lasting impression.
          </p>
          <div class="about-btn-container">
            <a href="#" class="about-btn">
              <span class="btn-text">ABOUT ME</span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
}
</script>

<style scoped>
.about {
  min-height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 6rem 0;
  position: relative;
}

.about-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  width: 100%;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 4rem;
  align-items: flex-start;
  max-width: 1200px;
  margin: 0 auto;
}

.about-left {
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  padding-top: 0;
}

.about-right {
  display: flex;
  flex-direction: column;
}

.about-title {
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: -0.02em;
  color: #E7E7E7;
  margin: 0;
  text-align: left;
}

.about-description {
  font-size: clamp(1.6rem, 2.5vw, 1.5rem);
  line-height: 1.7;
  color: #E7E7E7;
  margin-bottom: 10rem;
  font-weight: 400;
  text-align: left;
}

.about-btn-container {
  display: flex;
  justify-content: flex-start;
}

.about-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 150px;
  height: 150px;
  border: 2px solid #E7E7E7;
  border-radius: 50%;
  text-decoration: none;
  color: #E7E7E7;
  font-weight: 600;
  font-size: 0.9rem;
  letter-spacing: 0.05em;
  transition: all 0.4s ease;
  position: relative;
  background: transparent;
  overflow: hidden;
}

.about-btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background: linear-gradient(45deg, rgba(100, 255, 218, 0.1), rgba(0, 212, 170, 0.1)); */
  border-radius: 50%;
  opacity: 0;
  transition: opacity 0.4s ease;
}

/* .about-btn:hover::before {
  opacity: 1;
} */

.about-btn:hover {
  transform: scale(1.05);
}

.btn-text {
  position: relative;
  z-index: 2;
}

.about::after {
  content: '';
  position: absolute;
  bottom: 20%;
  left: 5%;
  width: 150px;
  height: 150px;
  /* background: radial-gradient(circle, rgba(0, 212, 170, 0.05) 0%, transparent 70%); */
  border-radius: 50%;
  animation: pulse 6s ease-in-out infinite reverse;
}

@keyframes pulse {
  0%,
  100% {
    transform: scale(1);
    opacity: 0.5;
  }
  50% {
    transform: scale(1.2);
    opacity: 0.8;
  }
}

@media (max-width: 768px) {
  .about {
    padding: 4rem 0;
  }

  .about-container {
    padding: 0 1rem;
  }

  .about-content {
    grid-template-columns: 1fr;
    gap: 3rem;
    text-align: center;
  }

  .about-left {
    justify-content: center;
  }

  .about-title {
    text-align: center;
  }

  .about-description {
    text-align: center;
    margin-bottom: 4rem;
  }

  .about-btn-container {
    justify-content: center;
  }

  .about-btn {
    width: 120px;
    height: 120px;
    font-size: 0.8rem;
  }
}
</style>