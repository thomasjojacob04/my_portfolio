<template>
  <section id="contact" class="contact">
    <div class="contact-container">
      <h2 class="contact-title">LET'S CONNECT!</h2>

      <form class="contact-form" @submit.prevent="handleSubmit">
        <div class="form-row">
          <div class="form-group">
            <label for="fullName">Full Name</label>
            <input
              type="text"
              id="fullName"
              v-model="form.fullName"
              placeholder="Enter full name"
              required
            />
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input
              type="email"
              id="email"
              v-model="form.email"
              placeholder="Enter email"
              required
            />
          </div>
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea
            id="message"
            v-model="form.message"
            placeholder="Leave me a message"
            rows="6"
            required
          ></textarea>
        </div>

        <div class="submit-section">
          <button type="submit" class="submit-btn">
            Send Message
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="arrow-icon">
              <path d="M20.0001 11.9998L4.00012 11.9998" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
              <path d="M15.0003 17C15.0003 17 20.0002 13.3176 20.0002 12C20.0002 10.6824 15.0002 7 15.0002 7" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
            </svg>
          </button>
        </div>
      </form>

      <div class="contact-info">
        <div class="contact-item">
          <div class="contact-header">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="contact-icon">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M14.92 2.78677C12.967 2.7377 11.033 2.7377 9.07999 2.78677L9.02182 2.78823C7.497 2.82651 6.27002 2.85732 5.2867 3.02857C4.2572 3.20786 3.42048 3.55174 2.71362 4.26129C2.00971 4.96787 1.66764 5.79256 1.49176 6.80537C1.32429 7.76974 1.29878 8.96677 1.26719 10.4496L1.26593 10.5084C1.24469 11.5047 1.24469 12.4952 1.26594 13.4916L1.26719 13.5503C1.29879 15.0332 1.32429 16.2302 1.49176 17.1946C1.66764 18.2074 2.00972 19.0321 2.71362 19.7386C3.42048 20.4482 4.2572 20.7921 5.2867 20.9714C6.27001 21.1426 7.49697 21.1734 9.02177 21.2117L9.07999 21.2132C11.033 21.2622 12.967 21.2622 14.92 21.2132L14.9782 21.2117C16.503 21.1734 17.73 21.1426 18.7133 20.9714C19.7428 20.7921 20.5795 20.4482 21.2864 19.7386C21.9903 19.0321 22.3324 18.2074 22.5082 17.1946C22.6757 16.2302 22.7012 15.0332 22.7328 13.5503L22.7341 13.4916C22.7553 12.4952 22.7553 11.5047 22.7341 10.5084L22.7328 10.4496C22.7012 8.96679 22.6757 7.76976 22.5082 6.80539C22.3324 5.79258 21.9903 4.96789 21.2864 4.26131C20.5795 3.55176 19.7428 3.20788 18.7133 3.02859C17.73 2.85733 16.503 2.82652 14.9782 2.78824L14.92 2.78677ZM7.38182 7.85449C7.02527 7.64368 6.56533 7.76183 6.35452 8.11838C6.14371 8.47494 6.26186 8.93488 6.61841 9.14569L9.56043 10.8851C10.4313 11.4 11.1827 11.7501 12.0001 11.7501C12.8175 11.7501 13.569 11.4 14.4398 10.8851L17.3818 9.14569C17.7384 8.93488 17.8565 8.47494 17.6457 8.11838C17.4349 7.76183 16.975 7.64368 16.6184 7.85449L13.6764 9.59392C12.832 10.0931 12.3831 10.2501 12.0001 10.2501C11.6171 10.2501 11.1682 10.0931 10.3238 9.59392L7.38182 7.85449Z" fill="#e7e7e7"></path>
            </svg>
            <span class="contact-label">Gmail</span>
          </div>
          <span class="contact-value">joeljacobjo04@gmail.com</span>
        </div>

        <div class="contact-item">
          <div class="contact-header">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="contact-icon">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M16.2305 1.34792C15.6076 1.26325 14.8464 1.25158 13.9548 1.25H10.0452C9.1536 1.25158 8.39242 1.26325 7.76946 1.34792C7.00417 1.45194 6.30442 1.68195 5.74096 2.25159C5.1775 2.82122 4.94999 3.52866 4.8471 4.30234C4.74993 5.03303 4.74996 5.95179 4.75 7.0463V16.9532C4.74996 18.0477 4.74993 18.9665 4.8471 19.6972C4.94999 20.4709 5.1775 21.1783 5.74096 21.7479C6.30442 22.3176 7.00417 22.5476 7.76946 22.6516C8.4922 22.7498 9.40098 22.7498 10.4836 22.7498H13.5163C14.5989 22.7498 15.5078 22.7498 16.2305 22.6516C16.9958 22.5476 17.6956 22.3176 18.259 21.7479C18.8225 21.1783 19.05 20.4709 19.1529 19.6972C19.2501 18.9665 19.25 18.0477 19.25 16.9532V7.04634C19.25 5.95182 19.2501 5.03304 19.1529 4.30234C19.05 3.52866 18.8225 2.82123 18.259 2.25159C17.6956 1.68195 16.9958 1.45194 16.2305 1.34792ZM8.02708 3.28394C8.4056 3.23249 8.86924 3.2138 9.47114 3.20703L9.6854 3.64025C9.84915 3.97134 10.1839 4.18047 10.55 4.18047H13.45C13.8162 4.18047 14.1509 3.97134 14.3146 3.64025L14.5289 3.20703C15.1308 3.2138 15.5944 3.23249 15.9729 3.28394C16.5238 3.35882 16.7476 3.4866 16.892 3.63256C17.0364 3.77851 17.1628 4.00473 17.2368 4.56168C17.3146 5.14673 17.3167 5.93294 17.3167 7.11229V16.885C17.3167 17.4596 17.3162 18.5899 17.3067 19H6.69333C6.68384 18.5899 6.68335 17.4596 6.68335 16.885V7.11229C6.68335 5.93294 6.6854 5.14673 6.76321 4.56168C6.83728 4.00473 6.96368 3.77851 7.10805 3.63256C7.25242 3.4866 7.47618 3.35882 8.02708 3.28394Z" fill="#e7e7e7"></path>
            </svg>
            <span class="contact-label">Mobile</span>
          </div>
          <span class="contact-value">+91 78931 62899</span>
        </div>

        <div class="contact-item">
          <div class="contact-header">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="contact-icon">
              <path d="M5.99794 16.4272C6.45239 16.7411 6.56638 17.3639 6.25254 17.8183C5.67012 18.6617 5.30838 19.2384 5.12382 19.6748C4.9515 20.0822 5.00571 20.1969 5.01938 20.2258L5.02019 20.2276C5.03784 20.2654 5.05874 20.3025 5.08287 20.3383C5.11863 20.3914 5.25287 20.5541 5.99963 20.6519C6.73331 20.748 7.76785 20.7501 9.2825 20.7501H14.718C16.2327 20.7501 17.2672 20.748 18.0009 20.6519C18.7477 20.5541 18.8819 20.3914 18.9177 20.3383L18.9804 20.2276L18.9812 20.2258C18.9948 20.1969 19.049 20.0822 18.8767 19.6748C18.6922 19.2384 18.3304 18.6617 17.748 17.8183C17.4342 17.3639 17.5482 16.7411 18.0026 16.4272C18.4571 16.1134 19.0799 16.2274 19.3937 16.6818C19.9658 17.5103 20.4433 18.2445 20.7187 18.8957C21.0028 19.5672 21.1437 20.3204 20.7931 21.0725C20.7311 21.2056 20.6586 21.3336 20.5766 21.4554C20.0379 22.2555 19.1424 22.5195 18.2607 22.635C17.3813 22.7502 16.2141 22.7501 14.793 22.7501H9.20757H9.20757C7.78644 22.7501 6.61928 22.7502 5.73987 22.635C4.85814 22.5195 3.96267 22.2555 3.4239 21.4554C3.34191 21.3336 3.26949 21.2056 3.20744 21.0725C2.85686 20.3204 2.99778 19.5672 3.2818 18.8957C3.55721 18.2445 4.03474 17.5103 4.60683 16.6818C4.92067 16.2274 5.54349 16.1134 5.99794 16.4272Z" fill="#e7e7e7"></path>
              <path fill-rule="evenodd" clip-rule="evenodd" d="M12.0005 1.25C8.94965 1.25 6.05208 3.10493 4.84158 6.01574C3.71464 8.72562 4.32729 11.035 5.59274 13.0023C6.62554 14.6079 8.13245 16.0411 9.47688 17.3198C9.73237 17.5628 9.98199 17.8002 10.2214 18.0322L10.223 18.0338C10.7003 18.4935 11.3377 18.75 12.0005 18.75C12.6633 18.75 13.3008 18.4935 13.7781 18.0337C14.0042 17.8159 14.2392 17.5932 14.4795 17.3655L14.4802 17.3648L14.4806 17.3645C15.8394 16.0769 17.367 14.6292 18.4106 13.0032C19.6745 11.034 20.285 8.72228 19.1595 6.01574C17.949 3.10493 15.0514 1.25 12.0005 1.25ZM12 6C10.3431 6 9 7.34315 9 9C9 10.6569 10.3431 12 12 12C13.6569 12 15 10.6569 15 9C15 7.34315 13.6569 6 12 6Z" fill="#e7e7e7"></path>
            </svg>
            <span class="contact-label">Location</span>
          </div>
          <span class="contact-value">Kottayam, Kerala</span>
        </div>
      </div>

      <footer class="footer">
        <div class="footer-content">
          <p class="copyright">Joel Jacob Thomas © 2025 All Rights Reserved</p>
          <div class="social-links">
            <a href="#" class="social-link">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="injected-svg" data-src="https://cdn.hugeicons.com/icons/linkedin-02-solid-rounded.svg?v=2.0" xmlns:xlink="http://www.w3.org/1999/xlink" role="img" color="#e7e7e7">
                <path d="M5 9H4.5C3.55719 9 3.08579 9 2.79289 9.29289C2.5 9.58579 2.5 10.0572 2.5 11V19.5C2.5 20.4428 2.5 20.9142 2.79289 21.2071C3.08579 21.5 3.55719 21.5 4.5 21.5H5C5.94281 21.5 6.41421 21.5 6.70711 21.2071C7 20.9142 7 20.4428 7 19.5V11C7 10.0572 7 9.58579 6.70711 9.29289C6.41421 9 5.94281 9 5 9Z" fill="#e7e7e7"></path>
                <path d="M7 4.75C7 5.99264 5.99264 7 4.75 7C3.50736 7 2.5 5.99264 2.5 4.75C2.5 3.50736 3.50736 2.5 4.75 2.5C5.99264 2.5 7 3.50736 7 4.75Z" fill="#e7e7e7"></path>
                <path d="M11.826 9H11C10.0572 9 9.58579 9 9.29289 9.29289C9 9.58579 9 10.0572 9 11V19.5C9 20.4428 9 20.9142 9.29289 21.2071C9.58579 21.5 10.0572 21.5 11 21.5H11.5C12.4428 21.5 12.9142 21.5 13.2071 21.2071C13.5 20.9142 13.5 20.4428 13.5 19.5L13.5001 16.0001C13.5001 14.3433 14.0281 13.0001 15.5879 13.0001C16.3677 13.0001 17 13.6717 17 14.5001V19.0001C17 19.9429 17 20.4143 17.2929 20.7072C17.5857 21.0001 18.0572 21.0001 19 21.0001H19.4987C20.4413 21.0001 20.9126 21.0001 21.2055 20.7073C21.4984 20.4145 21.4985 19.9432 21.4987 19.0006L21.5001 13.5002C21.5001 11.015 19.1364 9.00024 16.7968 9.00024C15.4649 9.00024 14.2767 9.65309 13.5001 10.674C13.5 10.0439 13.5 9.72893 13.3632 9.495C13.2765 9.34686 13.1531 9.22353 13.005 9.13687C12.7711 9 12.4561 9 11.826 9Z" fill="#e7e7e7"></path>
              </svg>
              
            </a>
            <a href="#" class="social-link">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="social-icon">
                <path d="M2.5 12C2.5 7.52166 2.5 5.28249 3.89124 3.89124C5.28249 2.5 7.52166 2.5 12 2.5C16.4783 2.5 18.7175 2.5 20.1088 3.89124C21.5 5.28249 21.5 7.52166 21.5 12C21.5 16.4783 21.5 18.7175 20.1088 20.1088C18.7175 21.5 16.4783 21.5 12 21.5C7.52166 21.5 5.28249 21.5 3.89124 20.1088C2.5 18.7175 2.5 16.4783 2.5 12Z" stroke="#e7e7e7" stroke-width="1.5" stroke-linejoin="round"></path>
                <path d="M16.5 12C16.5 14.4853 14.4853 16.5 12 16.5C9.51472 16.5 7.5 14.4853 7.5 12C7.5 9.51472 9.51472 7.5 12 7.5C14.4853 7.5 16.5 9.51472 16.5 12Z" stroke="#e7e7e7" stroke-width="1.5"></path>
                <path d="M17.5078 6.5L17.4988 6.5" stroke="#e7e7e7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
              </svg>
              
            </a>
            <a href="#" class="social-link">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" class="social-icon">
                <path d="M3 21L10.5484 13.4516M21 3L13.4516 10.5484M13.4516 10.5484L8 3H3L10.5484 13.4516M13.4516 10.5484L21 21H16L10.5484 13.4516" stroke="#e7e7e7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
              </svg>
              
            </a>
          </div>
        </div>
      </footer>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      form: {
        fullName: '',
        email: '',
        message: '',
      },
    }
  },
  methods: {
    handleSubmit() {
      // Handle form submission
      console.log('Form submitted:', this.form)
      // You can add actual form handling logic here
      alert('Message sent successfully!')

      // Reset form
      this.form = {
        fullName: '',
        email: '',
        message: '',
      }
    },
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Gilroy:wght@400;500;600;700;800;900&display=swap');

* {
  font-family: 'Gilroy', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Open Sans', 'Helvetica Neue', sans-serif;
}

.contact {
  padding: 6rem 0 2rem;
  min-height: 100vh;
}

.contact-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
}

.contact-title {
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 900;
  text-align: center;
  margin-bottom: 4rem;
  letter-spacing: -0.02em;
  background: #E7E7E7;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.contact-form {
  max-width: 1200px;
  margin: 0 auto 4rem;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-bottom: 2rem;
}

.form-group {
  display: flex;
  flex-direction: column;
}

.form-group label {
  font-size: 0.9rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: #E7E7E7;
  letter-spacing: 0.05em;
}

.form-group input,
.form-group textarea {
  background: rgba(255, 255, 255, 0);
  border: 1px solid #B4B4B4;
  padding: 1rem 1.5rem;
  color: white;
  font-size: 1rem;
  font-family: inherit;
  transition: all 0.3s ease;
  resize: vertical;
}

.submit-section {
  display: flex;
  justify-content: flex-end;
  margin-top: 3rem;
}

.submit-btn {
  background: #E7E7E7;
  color: #000000;
  padding: 1rem 2rem;
  border: none;
  font-size: 1rem;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  cursor: pointer;
  transition: all 0.3s ease;
  letter-spacing: 0.05em;
}

.arrow-icon {
  transition: transform 0.3s ease;
}

.submit-btn:hover .arrow-icon {
  transform: translateX(3px);
}

.contact-info {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 20rem;
  margin: 4rem 0;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
}

.contact-item {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.2rem;
  flex: 1;
}

.contact-header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.contact-icon {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
}

.contact-label {
  font-size: 0.9rem;
  font-weight: 600;
  color: #E7E7E7;
}

.contact-value {
  font-size: 1rem;
  font-weight: 500;
  color: #E7E7E7;
  padding-left: 0rem;
  line-height: 1.4;
  letter-spacing: 0.1rem;
}

.footer {
  margin-top: 4rem;
  padding-top: 2rem;
  border-top: 1px solid #E7E7E7;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 1rem;
}

.copyright {
  font-size: 0.9rem;
  color: #E7E7E7;
}

.social-links {
  display: flex;
  gap: 2rem;
}

.social-link {
  color: #E7E7E7;
  text-decoration: none;
  font-size: 0.9rem;
  transition: color 0.3s ease;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.social-icon {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
}

@media (max-width: 768px) {
  .contact {
    padding: 4rem 0 2rem;
  }

  .contact-container {
    padding: 0 1rem;
  }

  .form-row {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .submit-section {
    justify-content: center;
  }

  .contact-info {
    flex-direction: column;
    gap: 2.5rem;
    max-width: 100%;
  }

  .contact-item {
    align-items: flex-start;
  }

  .contact-value {
    padding-left: 2rem;
  }

  .footer-content {
    flex-direction: column;
    text-align: center;
  }

  .social-links {
    justify-content: center;
  }
}
</style>