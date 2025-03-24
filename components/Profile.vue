<template>
  <div>
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    
    <!-- About Section -->
    <section class="about">
      <div class="container">
        <div class="row">
          <!-- About Me Section -->
          <div class="col-md-6 mb-4" data-aos="fade-right">
            <h2 class="text-center mb-4">About Me</h2>
            <p>
              I'm <strong>Egi Danuarta</strong>, a passionate web developer based in Yogyakarta, Indonesia.
            </p>
            <p>
              As an enthusiastic student in the IT field, I specialize in web development and data science. My journey involves constant learning and staying up-to-date with the latest technologies to create innovative solutions.
            </p>
            <p>
              With strong communication skills and leadership experience from student organizations, I excel in collaborative environments. I believe in creating meaningful impact through technology while maintaining a user-centered approach.
            </p>
            <div class="social-links mt-4">
              <a href="https://github.com/praditus343" target="_blank" class="social-icon"><i class="fab fa-github"></i></a>
              <a href="https://www.linkedin.com/in/praditus-egi-danuarta/" target="_blank" class="social-icon"><i class="fab fa-linkedin"></i></a>
              <a href="https://www.instagram.com/egidanuarta17/" target="_blank" class="social-icon"><i class="fab fa-instagram"></i></a>
              <a href="https://egidanuarta.vercel.app/" target="_blank" class="social-icon"><i class="fas fa-globe"></i></a>
            </div>
            <button class="btn btn-primary" @click="downloadResume">
              <i class="fas fa-download mr-2"></i>Download Resume
            </button>
          </div>
          <!-- Profile Image Section -->
          <div class="col-md-6 mb-4 d-flex justify-content-center align-items-center" data-aos="fade-left">
            <div class="profile-container">
              <img src="/assets/img/1.png" alt="Egi Danuarta" class="img-fluid rounded-circle shadow-lg" />
            </div>
          </div>
        </div>
        <!-- Skills Section -->
        <div class="skills mt-5" data-aos="fade-up">
          <h2 class="text-center mb-4">Skills</h2>
          <div class="row">
            <div class="col-md-4 mb-4">
              <div class="skill-card">
                <div class="skill-icon">
                  <i class="fas fa-laptop-code"></i>
                </div>
                <h4>Web Development</h4>
                <p>Expert in modern web technologies including Vue.js, React, and Node.js. Focused on creating responsive and performant applications.</p>
                <div class="skill-progress">
                  <div class="progress">
                    <div class="progress-bar" role="progressbar" style="width: 90%"></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-md-4 mb-4">
              <div class="skill-card">
                <div class="skill-icon">
                  <i class="fas fa-chart-line"></i>
                </div>
                <h4>Data Science</h4>
                <p>Proficient in data analysis, machine learning, and statistical modeling using Python, Pandas, and scikit-learn.</p>
                <div class="skill-progress">
                  <div class="progress">
                    <div class="progress-bar" role="progressbar" style="width: 85%"></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-md-4 mb-4">
              <div class="skill-card">
                <div class="skill-icon">
                  <i class="fas fa-mobile-alt"></i>
                </div>
                <h4>Responsive Design</h4>
                <p>Skilled in creating adaptive layouts using modern CSS frameworks and best practices for optimal user experience across all devices.</p>
                <div class="skill-progress">
                  <div class="progress">
                    <div class="progress-bar" role="progressbar" style="width: 88%"></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- Contact Section -->
        <div class="contact mt-5" data-aos="fade-up">
          <h2 class="text-center mb-4">Get In Touch</h2>
          <div class="row justify-content-center">
            <div class="col-md-8">
              <div class="contact-card">
                <div class="contact-info">
                  <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <a href="mailto:egidanuarta17@gmail.com">egidanuarta17@gmail.com</a>
                  </div>
                  <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <a href="tel:+6285700120940">+62 857-0012-0940</a>
                  </div>
                  <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Yogyakarta, Indonesia</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'

export default {
  name: 'About',
  components: {
    Navbar,
    Footer
  },
  mounted() {
    // Initialize AOS
    if (typeof AOS !== 'undefined') {
      AOS.init({
        duration: 1000,
        once: true
      });
    }
  },
  methods: {
    downloadResume() {
      window.open('https://drive.google.com/file/d/1rVdFp31R-hKD4uKZzj3KfHLZnfwj1knC/view?usp=sharing', '_blank');
    }
  }
}
</script>

<style scoped>
.about {
  padding: 80px 0;
  background: #0f172a;
  color: #fff;
}

.profile-container {
  position: relative;
  width: 250px;
  height: 250px;
  border-radius: 50%;
  overflow: hidden;
  border: 4px solid #01c879;
  transition: all 0.3s ease;
}

.profile-container:hover {
  transform: scale(1.05);
  border-color: #019d6b;
}

.about img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: all 0.3s ease;
}

h2 {
  color: #cbd5e1;
  font-size: 2.2rem;
  font-weight: 700;
  margin-bottom: 30px;
  position: relative;
  display: inline-block;
}

h2::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 50px;
  height: 3px;
  background: #01c879;
}

p {
  color: #cbd5e1;
  font-size: 1.1rem;
  line-height: 1.8;
  margin-bottom: 1.2rem;
}

.social-links {
  display: flex;
  gap: 20px;
  justify-content: center;
  margin-bottom: 20px;
}

.social-icon {
  color: #cbd5e1;
  font-size: 1.5rem;
  transition: all 0.3s ease;
}

.social-icon:hover {
  color: #01c879;
  transform: translateY(-3px);
}

.btn-primary {
  background-color: #01c879;
  border-color: #01c879;
  border-radius: 25px;
  padding: 12px 25px;
  font-size: 1.1rem;
  margin-top: 20px;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(1, 200, 121, 0.2);
}

.btn-primary:hover {
  background-color: #019d6b;
  border-color: #019d6b;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(1, 200, 121, 0.3);
}

.skill-card {
  background: #1e293b;
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  text-align: center;
  transition: all 0.3s ease;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.skill-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
}

.skill-icon {
  font-size: 2.8rem;
  color: #01c879;
  margin-bottom: 20px;
}

.skill-card h4 {
  color: #cbd5e1;
  font-size: 1.3rem;
  margin-bottom: 15px;
  font-weight: 600;
}

.skill-card p {
  color: #9ca3af;
  font-size: 1rem;
  flex-grow: 1;
}

.skill-progress {
  margin-top: 15px;
}

.progress {
  height: 8px;
  background: #2d3748;
  border-radius: 4px;
  overflow: hidden;
}

.progress-bar {
  background: #01c879;
  transition: width 1.5s ease-in-out;
}

.contact-card {
  background: #1e293b;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 15px;
  font-size: 1.1rem;
}

.contact-item i {
  color: #01c879;
  font-size: 1.3rem;
}

.contact-item a, .contact-item span {
  color: #cbd5e1;
  text-decoration: none;
  transition: color 0.3s ease;
}

.contact-item a:hover {
  color: #01c879;
}

@media (max-width: 767px) {
  .about {
    padding: 50px 0;
  }

  h2 {
    font-size: 1.8rem;
  }

  .profile-container {
    width: 200px;
    height: 200px;
  }

  .skill-card {
    padding: 20px;
  }

  .contact-card {
    padding: 20px;
  }

  .contact-item {
    font-size: 1rem;
  }
}
</style>
