<template>
  <div>
    <!-- Include Bootstrap and Font Awesome -->
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    
    <section class="hero">
      <div class="container">
        <div class="main-body">
          <div class="row gutters-sm">
            
            <!-- Sidebar Section -->
            <div class="col-md-4 mb-3">
              <div class="card profile-card">
                <div class="card-body text-center">
                  <img src="/assets/img/1.png" alt="Admin" class="rounded-circle profile-image" width="150">
                  <div class="profile-info mt-3">
                    <h4>Praditus Egi Danuarta</h4>
                    <p class="text-secondary">IT Enthusiast</p>
                    <div class="profile-buttons">
                      <a href="https://www.instagram.com/egidanuarta17/" class="btn btn-primary" target="_blank">Follow</a>
                      <a href="https://mail.google.com/mail/u/0/?view=cm&tf=1&fs=1&to=egidanuarta17@gmail.com" class="btn btn-outline-primary" target="_blank">Message</a>
                    </div>
                    <p class="text-muted text-container">
                      I am an IT student who is particularly interested in data science and web development. I enjoy picking up new skills and mastering new technology.
                    </p>
                  </div>
                </div>
              </div>

              <!-- Social Media Links Card -->
              <div class="card mt-3 social-links-card">
                <ul class="list-group list-group-flush">
                  <li class="list-group-item">
                    <a href="https://egidanuarta.vercel.app/" target="_blank" class="d-flex align-items-center">
                      <i class="fab fa-globe mr-3"></i> Website
                      <span class="ml-auto text-secondary">https://egidanuarta.vercel.app/</span>
                    </a>
                  </li>
                  <li class="list-group-item">
                    <a href="https://github.com/praditus343" target="_blank" class="d-flex align-items-center">
                      <i class="fab fa-github mr-3"></i> Github
                      <span class="ml-auto text-secondary">praditus343</span>
                    </a>
                  </li>
                  <li class="list-group-item">
                    <a href="https://www.instagram.com/egidanuarta17/" target="_blank" class="d-flex align-items-center">
                      <i class="fab fa-instagram mr-3"></i> Instagram
                      <span class="ml-auto text-secondary">@egidanuarta17</span>
                    </a>
                  </li>
                  <li class="list-group-item">
  <a href="https://www.instagram.com/egidanuarta17/" target="_blank" class="d-flex align-items-center">
    <i class="fas fa-times mr-3"></i> X
    <span class="ml-auto text-secondary">@egidanuarta17</span>
  </a>
</li>

                  <li class="list-group-item">
                    <a href="https://www.facebook.com/egidanuarta17" target="_blank" class="d-flex align-items-center">
                      <i class="fab fa-facebook mr-3"></i> Facebook
                      <span class="ml-auto text-secondary">egidanuarta17</span>
                    </a>
                  </li>
                </ul>
              </div>
            </div>

            <!-- Main Content Section -->
            <div class="col-md-8">
              <div class="card mb-3">
                <div class="card-body">
                  <div class="info-row">
                    <div class="row">
                      <div class="col-sm-3">
                        <h6>Full Name</h6>
                      </div>
                      <div class="col-sm-9 text-secondary">
                        Praditus Egi Danuarta
                      </div>
                    </div>
                    <hr>
                    <div class="row">
                      <div class="col-sm-3">
                        <h6>Email</h6>
                      </div>
                      <div class="col-sm-9 text-secondary">
                        egidanuarta17@gmail.com
                      </div>
                    </div>
                    <hr>
                    <div class="row">
                      <div class="col-sm-3">
                        <h6>Phone</h6>
                      </div>
                      <div class="col-sm-9 text-secondary">
                        (+62) 857-0012-0940
                      </div>
                    </div>
                    <hr>
                    <div class="row">
                      <div class="col-sm-3">
                        <h6>Mobile</h6>
                      </div>
                      <div class="col-sm-9 text-secondary">
                        (+62) 857-0012-0940
                      </div>
                    </div>
                    <hr>
                    <div class="row">
                      <div class="col-sm-3">
                        <h6>Address</h6>
                      </div>
                      <div class="col-sm-9 text-secondary">
                        Sleman, Yogyakarta
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Skills Section -->
              <div class="card mb-2">
                <div class="card-body">
                  <h6 class="d-flex align-items-center mb-4">
                    <i class="fas fa-cogs mr-3 text-primary"></i>
                    <span>Skills</span>
                  </h6>
                  <div class="row skills-grid">
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-html5 fa-2x text-danger"></i>
                      <p>HTML5</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-css3-alt fa-2x text-info"></i>
                      <p>CSS3</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-js fa-2x text-warning"></i>
                      <p>JavaScript</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-node fa-2x text-success"></i>
                      <p>Node.js</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fas fa-server fa-2x text-muted"></i>
                      <p>Server</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fas fa-database fa-2x text-primary"></i>
                      <p>Database</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-react fa-2x text-info"></i>
                      <p>React.js</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-vuejs fa-2x text-success"></i>
                      <p>Vue.js</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fab fa-python fa-2x text-info"></i>
                      <p>Python</p>
                    </div>
                    <div class="col-5 col-md-2 mb-5 skill-card">
                      <i class="fas fa-express fa-2x text-success"></i>
                      <p>Express.js</p>
                    </div>
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
export default {
  name: 'Profile'
}
</script>

<style scoped>
.hero {
  padding: 40px 0;
  background: #0f172a;
  color: #fff;
  min-height: 100vh;
}

.card {
  background: #1e293b;
  border-radius: 15px;
  border: none;
  margin-bottom: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.profile-image {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border: 3px solid #01c879;
  margin-bottom: 20px;
}

.profile-info h4 {
  color: #fff;
  margin-bottom: 10px;
}

.profile-buttons {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  margin: 15px 0;
}

.btn {
  padding: 8px 20px;
  border-radius: 20px;
  font-weight: 500;
}

.btn-primary {
  background-color: #01c879;
  border-color: #01c879;
}

.btn-outline-primary {
  color: #01c879;
  border-color: #01c879;
}

.text-container {
  max-width: 100%;
  padding: 0 15px;
  text-align: center;
  color: #cbd5e1;
}

.social-links-card .list-group-item {
  background: transparent;
  border-color: rgba(255, 255, 255, 0.1);
  padding: 15px;
}

.social-links-card .list-group-item a {
  text-decoration: none;
  color: #fff;
}

.social-links-card .list-group-item:hover {
  background-color: #334155;
}

.info-row .row {
  margin-bottom: 15px;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

.skill-card {
  background: #334155;
  padding: 15px;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s, background-color 0.3s, box-shadow 0.3s;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
}

.skill-card:hover {
  background-color: #01c879;
  transform: scale(1.1);
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
}

.skill-card i {
  transition: transform 0.3s;
}

.skill-card:hover i {
  transform: scale(1.2);
}

.skill-card p {
  margin-top: 10px;
  font-size: 1rem;
  color: #cbd5e1;
}

</style>