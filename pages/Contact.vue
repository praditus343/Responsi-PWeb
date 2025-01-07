<template>
  <div>
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <Navbar />
    <section class="contact">
      <div class="container">
        <div class="row">
          <div class="col-md-12 mb-5">
            <h2 class="text-center mb-5">Contact Me</h2>
          </div>
          <div class="col-md-6 mb-4">
            <!-- Contact Info Card -->
            <div class="contact-info">
              <h3>Contact Details</h3>
              <ul class="list-unstyled">
                <li><i class="fas fa-envelope"></i> <a href="mailto:egidanuarta17@gmail.com">egidanuarta17@gmail.com</a></li>
                <li><i class="fas fa-phone"></i> (+62) 857-0012-0940</li>
                <li><i class="fas fa-map-marker-alt"></i> Sleman, Yogyakarta</li>
                <li><i class="fab fa-github"></i> <a href="https://github.com/praditus343" target="_blank">github.com/praditus343</a></li>
                <li><i class="fab fa-twitter"></i> <a href="https://twitter.com/egidanuarta17" target="_blank">@egidanuarta17</a></li>
                <li><i class="fab fa-instagram"></i> <a href="https://www.instagram.com/egidanuarta17/" target="_blank">@egidanuarta17</a></li>
              </ul>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <!-- Contact Form Card -->
            <div class="contact-form">
              <form @submit.prevent="sendMessage">
                <div class="form-group">
                  <label for="name">Name</label>
                  <input
                    type="text"
                    class="form-control"
                    id="name"
                    v-model="form.name"
                    placeholder="Your Name"
                    required
                    :class="{'is-invalid': formErrors.name}"
                  />
                  <div v-if="formErrors.name" class="invalid-feedback">{{ formErrors.name }}</div>
                </div>
                <div class="form-group">
                  <label for="email">Email</label>
                  <input
                    type="email"
                    class="form-control"
                    id="email"
                    v-model="form.email"
                    placeholder="Your Email"
                    required
                    :class="{'is-invalid': formErrors.email}"
                  />
                  <div v-if="formErrors.email" class="invalid-feedback">{{ formErrors.email }}</div>
                </div>
                <div class="form-group">
                  <label for="message">Message</label>
                  <textarea
                    class="form-control"
                    id="message"
                    v-model="form.message"
                    rows="4"
                    placeholder="Your Message"
                    required
                    :class="{'is-invalid': formErrors.message}"
                  ></textarea>
                  <div v-if="formErrors.message" class="invalid-feedback">{{ formErrors.message }}</div>
                </div>
                <button
                  type="submit"
                  class="btn btn-primary"
                  :disabled="isSubmitting"
                >
                  <span v-if="isSubmitting">Sending...</span>
                  <span v-else>Send</span>
                </button>
              </form>
            </div>
          </div>
        </div>
        <!-- Map Section Below Cards -->
        <div class="row">
          <div class="col-md-12">
            <div class="map mt-4">
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15875.64419141374!2d110.4078221!3d-7.758512!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e7a3d6f9e0c9c5b%3A0xa9fa7b1a11cbb2e8!2sSleman%2C%20Yogyakarta!5e0!3m2!1sen!2sid!4v1688991851345!5m2!1sen!2sid"
                width="100%"
                height="300"
                style="border:0;"
                allowfullscreen=""
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
                title="Google Maps"
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      },
      isSubmitting: false,
      formErrors: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    validateForm() {
      this.formErrors.name = this.form.name ? '' : 'Name is required';
      this.formErrors.email = this.isValidEmail(this.form.email) ? '' : 'Valid email is required';
      this.formErrors.message = this.form.message ? '' : 'Message cannot be empty';
      return !Object.values(this.formErrors).some(error => error);
    },
    isValidEmail(email) {
      const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
      return emailPattern.test(email);
    },
    sendMessage() {
      if (!this.validateForm()) {
        return;
      }

      this.isSubmitting = true;
      
      // Kirim email menggunakan EmailJS
      const templateParams = {
        name: this.form.name,
        email: this.form.email,
        message: this.form.message
      };

      emailjs.send('service_hcn1hln', 'template_gn0lv1m', templateParams, 'ARhuSalaRawx81DAt')
        .then((response) => {
          alert('Message sent! Thank you for contacting me.');
          this.isSubmitting = false;
          this.form.name = '';
          this.form.email = '';
          this.form.message = '';
        }, (error) => {
          alert('Failed to send message. Please try again later.');
          this.isSubmitting = false;
        });
    }
  }
}
</script>

<style scoped>
.contact {
  padding: 80px 0;
  background: #0f172a;
  color: #fff;
}

.contact h2 {
  color: #cbd5e1;
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 40px;
  position: relative;
}

.contact h2::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 4px;
  background-color: #01c879;
  border-radius: 2px;
}

.contact-form {
  background: #1e293b;
  border-radius: 15px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  padding: 30px;
  transition: all 0.3s ease;
  min-height: 400px;
}

.contact-info {
  background: #1e293b;
  border-radius: 15px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  padding: 75px;
  transition: all 0.3s ease;
  min-height: 400px;
}

.contact-form:hover, .contact-info:hover {
  box-shadow: 0 12px 20px rgba(0, 0, 0, 0.3);
}

.contact-form .form-group label {
  color: #cbd5e1;
}

.contact-form .form-control {
  border-radius: 10px;
  background: #1e293b;
  color: #cbd5e1;
  border: 1px solid #374151;
}

.contact-form .form-control::placeholder {
  color: #9ca3af;
}

.contact-form .btn-primary {
  background-color: #01c879;
  border-color: #01c879;
  border-radius: 10px;
  padding: 12px;
  font-size: 1.1rem;
}

.contact-form .btn-primary:hover {
  background-color: #019d6b;
  border-color: #019d6b;
}

.contact-info h4 {
  margin-bottom: 20px;
  color: #cbd5e1;
}

.contact-info ul {
  padding-left: 0;
  list-style: none;
}

.contact-info li {
  margin-bottom: 15px;
  color: #cbd5e1;
  font-size: 1.1rem;
  display: flex;
  align-items: center;
}

.contact-info li i {
  color: #01c879;
  margin-right: 10px;
}

.map {
  margin-top: 20px;
  border-radius: 10px;
  overflow: hidden;
}

.is-invalid {
  border-color: #dc3545;
}

.invalid-feedback {
  color: #dc3545;
  font-size: 0.875rem;
}

@media (max-width: 767px) {
  .contact h2 {
    font-size: 2rem;
  }

  .contact-form .btn-primary {
    font-size: 1rem;
  }

  .contact-form, .contact-info {
    margin-bottom: 30px;
  }
}
</style>
