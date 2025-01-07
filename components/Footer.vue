<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <!-- Logo and Description -->
        <div class="footer-section about">
          <h5 class="footer-title">Praditus Egi Danuarta</h5>
          <p class="profile-description">
            I am a student with a keen interest in the field of IT, particularly in web development and data science. I am always eager to learn new technologies and enhance my skills in this domain.
          </p>
        </div>

        <!-- Quick Links -->
        <div class="footer-section links">
          <h5 class="footer-title">Quick Links</h5>
          <ul class="footer-links">
            <li><NuxtLink to="/" class="footer-link">Home</NuxtLink></li>
            <li><NuxtLink to="/projects" class="footer-link">Projects</NuxtLink></li>
            <li><NuxtLink to="/about" class="footer-link">About</NuxtLink></li>
            <li><NuxtLink to="/contact" class="footer-link">Contact</NuxtLink></li>
          </ul>
        </div>

        <!-- Social Media -->
        <div class="footer-section social">
          <h5 class="footer-title">Follow Us</h5>
          <div class="social-links">
            <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
            <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
            <a href="https://www.instagram.com/egidanuarta17/" class="social-link"><i class="fab fa-instagram"></i></a>
            <a href="https://www.linkedin.com/in/praditus-egi-danuarta/" class="social-link"><i class="fab fa-linkedin-in"></i></a>
            <a href="https://github.com/praditus343" class="social-link"><i class="fab fa-github"></i></a>
          </div>
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
  name: "Footer",
};
</script>

<style scoped>
/* Footer Base Styles */
.footer {
  background-color: #0f172a;
  color: white;
  padding: 30px 15px;
  font-family: "Arial", sans-serif;
}

.footer .container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  text-align: center;
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100%;
  gap: 20px;
}

.footer-section {
  flex: 1;
  min-width: 200px;
  margin: 10px;
  padding-top: 15px;
  position: relative;
}

.footer-section::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: #01c879; /* Garis di bagian atas */
}

.footer-title {
  font-size: 1.5rem;
  margin-bottom: 15px;
  color: #01c879;
}

.profile-description {
  font-size: 1rem;
  line-height: 1.6;
  text-align: justify;
  margin: 0 auto;
  max-width: 300px;
}

.footer-links {
  list-style: none;
  padding: 0;
}

.footer-links li {
  margin: 5px 0;
}

.footer-link {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s ease;
}

.footer-link:hover {
  color: #01c879;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 15px;
}

.social-link {
  color: white;
  font-size: 1.5rem;
  transition: color 0.3s ease;
}

.social-link:hover {
  color: #01c879;
}

/* Footer Bottom */
.footer-bottom {
  width: 100%;
  text-align: center;
  margin-top: 20px;
  padding-top: 15px;
  border-top: 2px solid #01c879; /* Garis di bagian atas footer-bottom */
  font-size: 0.9rem;
}

/* Responsive Styles */
@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
  }

  .footer-section {
    text-align: center;
    margin: 0 0 20px 0;
  }

  .footer-section::before {
    left: 50%;
    transform: translateX(-50%);
    width: 80%; /* Garis menyesuaikan pada layar kecil */
  }
}
</style>
