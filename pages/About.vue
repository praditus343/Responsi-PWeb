<template>
  <div>
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <!-- Navbar -->
    <Navbar />
    
    <!-- About Section -->
    <section class="about">
      <div class="container">
        <div class="row">
          <!-- About Me Section -->
          <div class="col-md-6 mb-4">
            <h2 class="text-center mb-4">About Me</h2>
            <p>
              I’m <strong>Egi Danuarta</strong>, a web developer based in Yogyakarta, Indonesia.
            </p>
            <p>
              I am a student with a keen interest in the field of IT, particularly in web development and data science. I am always eager to learn new technologies and enhance my skills in this domain.
            </p>
            <p>
              In addition to my technical expertise, I possess excellent communication skills and thrive in collaborative environments. My experience in student organizations has equipped me with strong interpersonal and leadership abilities. I am confident that these skills will prove invaluable in my future career.
            </p>
            <button class="btn btn-primary" @click="downloadResume">Download Resume</button>
          </div>
          <!-- Profile Image Section -->
          <div class="col-md-6 mb-4 d-flex justify-content-center">
            <img src="/assets/img/1.png" alt="Egi Danuarta" class="img-fluid rounded-circle shadow-lg" />
          </div>
        </div>
        <!-- Skills Section -->
        <div class="skills mt-5">
          <h2 class="text-center mb-4">Skills</h2>
          <div class="row">
            <div class="col-md-4 mb-4">
              <div class="skill-card">
                <div class="skill-icon">
                  <i class="fas fa-laptop-code"></i>
                </div>
                <h4>Web Development</h4>
                <p>Experienced in building websites with modern technologies like Vue.js, React, and Angular.</p>
              </div>
            </div>
<div class="col-md-4 mb-4">
  <div class="skill-card">
    <div class="skill-icon">
      <i class="fas fa-chart-line"></i>
    </div>
    <h4>Data Science</h4>
    <p>Proficient in data analysis, machine learning, and working with large datasets using tools like Python.</p>
  </div>
</div>

            <div class="col-md-4 mb-4">
              <div class="skill-card">
                <div class="skill-icon">
                  <i class="fas fa-mobile-alt"></i>
                </div>
                <h4>Responsive Design</h4>
                <p>Creating responsive layouts and interfaces for all devices and screen sizes involves designing and developing web pages that</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Footer -->
    <Footer />
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
  methods: {
    downloadResume() {
      // Menggunakan link Google Drive
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

.about img {
  width: 100%;
  max-width: 250px;
  height: auto;
}

h2 {
  color: #cbd5e1;
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 30px;
}

p {
  color: #cbd5e1;
  font-size: 1.1rem;
  line-height: 1.6;
}

.btn-primary {
  background-color: #01c879;
  border-color: #01c879;
  border-radius: 10px;
  padding: 12px;
  font-size: 1.1rem;
  margin-top: 20px;
}

.btn-primary:hover {
  background-color: #019d6b;
  border-color: #019d6b;
}

.skills h2 {
  color: #cbd5e1;
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 30px;
}

.skill-card {
  background: #1e293b;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  text-align: center;
  transition: all 0.3s ease;
}

.skill-card:hover {
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
}

.skill-icon {
  font-size: 2.5rem;
  color: #01c879;
  margin-bottom: 15px;
}

.skill-card h4 {
  color: #cbd5e1;
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.skill-card p {
  color: #9ca3af;
  font-size: 1rem;
}

@media (max-width: 767px) {
  h2 {
    font-size: 1.5rem;
  }

  .btn-primary {
    font-size: 1rem;
  }
}
</style>
