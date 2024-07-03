<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <!-- Logo and Description -->
        <div class="footer-section about">
          <h5 class="footer-title">Praditus Egi Danuarta </h5>
          <div class="profile-description">
          <p>I am a student with a keen interest in the field of IT, particularly in web development and data science. I am always eager to learn new technologies and enhance my skills in this domain.</p>
          </div>
        </div>

        <!-- Quick Links -->
        <div class="footer-section links">
          <h5 class="footer-title">Quick Links</h5>
          <NuxtLink to="/" class="footer-link">Home</NuxtLink>
          <NuxtLink to="/projects" class="footer-link">Projects</NuxtLink>
          <NuxtLink to="/about" class="footer-link">About</NuxtLink>
          <NuxtLink to="/contact" class="footer-link">Contact</NuxtLink>
        </div>

        <!-- Social Media -->
        <div class="footer-section social">
          <h5 class="footer-title">Follow Us</h5>
          <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
          <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
          <a href="https://www.instagram.com/egidanuarta17/" class="social-link"><i class="fab fa-instagram"></i></a>
          <a href="https://www.linkedin.com/in/praditus-egi-danuarta/" class="social-link"><i class="fab fa-linkedin-in"></i></a>
          <a href="https://github.com/praditus343" class="social-link"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 | Designed by Praditus Egi Danuarta</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>

.profile-description p {
  text-align: justify;
}

.footer {
  background-color: #0f172a;
  color: white;
  padding: 20px 0;
}

.footer .container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
  width: 100%;
  text-align: center;
  margin-top: 20px;
  border-top: 1px solid #01c879;
  padding-top: 10px;
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100%;
}

.footer-section {
  flex: 1;
  margin: 10px;
}

.footer-title {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: #01c879;
}

.footer-link {
  display: block;
  margin-bottom: 5px;
  color: white;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-link:hover {
  color: #01c879;
}

.social-link {
  color: white;
  margin-right: 10px;
  font-size: 1.2rem;
  transition: color 0.3s;
}

.social-link:hover {
  color: #01c879;
}

.footer-bottom {
  width: 100%;
  text-align: center;
  margin-top: 20px;
  border-top: 1px solid #01c879;
  padding-top: 10px;
}
</style>
