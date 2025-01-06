<template>
  <div>
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <section class="hero">
      <div class="container">
        <div class="main-body">
          <div class="row gutters-sm">
            <!-- Sidebar Section -->
            <div class="col-md-4 mb-3">
              <div class="card">
                <div class="card-body">
                  <div class="d-flex flex-column align-items-center text-center">
                    <!-- Profile Picture -->
                    <img src="/static/assets/img/1.png" alt="Admin" class="rounded-circle" width="150">
                    <div class="mt-1">
                      <h4>Praditus Egi Danuarta</h4>
                      <p class="text-secondary mb-1">IT Enthusiast</p>
                      <a href="https://www.instagram.com/egidanuarta17/" class="btn btn-primary mb-2">Follow</a>
                      <a href="https://mail.google.com/mail/u/0/?view=cm&tf=1&fs=1&to=egidanuarta17@gmail.com" class="btn btn-outline-primary mb-2">Message</a>
                      <!-- Add a brief description -->
                      <p class="text-muted mt-2 text-container">
                        I am a student with a keen interest in the field of IT, particularly in web development and data science. I am always eager to learn new technologies and enhance my skills in this domain.</p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="card mt-3">
                <ul class="list-group list-group-flush">
                  <!-- Social Media Links -->
                  <li class="list-group-item d-flex justify-content-between align-items-center flex-wrap">
                    <h6 class="mb-0"><i class="feather feather-globe mr-2 icon-inline"></i>Website</h6>
                    <span class="text-secondary">https://bootdey.com</span>
                  </li>
                  <li class="list-group-item d-flex justify-content-between align-items-center flex-wrap">
                    <h6 class="mb-0"><i class="feather feather-github mr-2 icon-inline"></i>Github</h6>
                    <span class="text-secondary">praditus343</span>
                  </li>
                  <li class="list-group-item d-flex justify-content-between align-items-center flex-wrap">
                    <h6 class="mb-0"><i class="feather feather-twitter mr-2 icon-inline text-info"></i>Twitter</h6>
                    <span class="text-secondary">@egidanuarta17</span>
                  </li>
                  <li class="list-group-item d-flex justify-content-between align-items-center flex-wrap">
                    <h6 class="mb-0"><i class="feather feather-instagram mr-2 icon-inline text-danger"></i>Instagram</h6>
                    <span class="text-secondary">@egidanuarta17</span>
                  </li>
                  <li class="list-group-item d-flex justify-content-between align-items-center flex-wrap">
                    <h6 class="mb-0"><i class="feather feather-facebook mr-2 icon-inline text-primary"></i>Facebook</h6>
                    <span class="text-secondary">egidanuarta17</span>
                  </li>
                </ul>
              </div>
            </div>
            <!-- Main Content Section -->
            <div class="col-md-8">
              <div class="card mb-3">
                <div class="card-body">
                  <!-- Personal Information -->
                  <div class="row">
                    <div class="col-sm-3">
                      <h6 class="mb-0">Full Name</h6>
                    </div>
                    <div class="col-sm-9 text-secondary">
                      Praditus Egi Danuarta
                    </div>
                  </div>
                  <hr>
                  <div class="row">
                    <div class="col-sm-3">
                      <h6 class="mb-0">Email</h6>
                    </div>
                    <div class="col-sm-9 text-secondary">
                      egidanuarta17@gmail.com
                    </div>
                  </div>
                  <hr>
                  <div class="row">
                    <div class="col-sm-3">
                      <h6 class="mb-0">Phone</h6>
                    </div>
                    <div class="col-sm-9 text-secondary">
                      (+62) 857-0012-0940
                    </div>
                  </div>
                  <hr>
                  <div class="row">
                    <div class="col-sm-3">
                      <h6 class="mb-0">Mobile</h6>
                    </div>
                    <div class="col-sm-9 text-secondary">
                        (+62) 857-0012-0940
                    </div>
                  </div>
                  <hr>
                  <div class="row">
                    <div class="col-sm-3">
                      <h6 class="mb-0">Address</h6>
                    </div>
                    <div class="col-sm-9 text-secondary">
                      Sleman, Yogyakarta
                    </div>
                  </div>
                  <hr>
                </div>
              </div>
              <div class="row gutters-sm">
                <!-- Skills Section with Icons -->
                <div class="col-md-12">
                            <div class="card mb-3">
                            <div class="card-body mb-4">
                            <!-- Skills Section Header -->
                            <h6 class="d-flex align-items-center mb-5">
                                <i class="fas fa-cogs fa-3x mr-4 text-primary"></i>
                                <span>Skills</span>
                            </h6>
                            <div class="row">
                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-html5 fa-3x mb-2 text-danger"></i>

                                </div>
                                </div>
                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-css3-alt fa-3x mb-2 text-info"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-js fa-3x mb-2 text-warning"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-node fa-3x mb-2 text-green"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fas fa-server fa-3x mb-2 text-muted"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fas fa-database fa-3x mb-2 text-blue"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fas fa-database fa-3x mb-2 text-green"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-2">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-react fa-3x mb-2 text-blue"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-3">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-vuejs fa-3x mb-2 text-green"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-3">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-figma fa-3x mb-2 text-purple"></i>
                                </div>
                                </div>
                                
                                <div class="col-md-3 mb-3">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-python fa-3x mb-2 text-blue"></i>
                                </div>
                                </div>

                                <div class="col-md-3 mb-3">
                                <div class="skill-card text-center p-3 bg-dark text-light rounded">
                                    <i class="fab fa-cuttlefish fa-3x mb-2 text-blue"></i>
                                </div>
                                </div>

                            </div>
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
  text-align: center;
  padding: 100px 0;
  background: #0f172a;
  color: #fff;
}

.hero .card {
  background: #1e293b;
  border-radius: 10px;
}

.hero .card-body {
  color: #cbd5e1;
}

/* Gaya untuk tombol */
.btn {
  margin-right: 10px; /* Jarak antara tombol Follow dan Message */
}

/* Gaya untuk tombol saat hover */
.btn-primary:hover, .btn-outline-primary:hover {
  opacity: 0.9; /* Sedikit transparansi pada hover */
}

/* Gaya untuk link tombol */
a.btn {
  display: inline-block; /* Agar tombol dapat diratakan dalam baris */
}

/* Jarak antara tombol dengan konten berikutnya */
.mt-2 {
  margin-top: 0.5rem;
}

/* Responsif */
@media (max-width: 767px) {
  .btn {
    margin-right: 5px; /* Jarak lebih kecil pada layar kecil */
  }
}


.hero .list-group-item {
  background: #1e293b;
  border: none;
}

.hero .list-group-item:hover {
  background: #334155;
}

.icon-inline {
  width: 24px;
  height: 24px;
  stroke-width: 2;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin-bottom: 10px;
}

.list-unstyled {
  padding-left: 0;
}

.text-muted {
  color: #6b7280 !important;
}

.progress {
  height: 20px;
  border-radius: 10px;
}

.progress-bar {
  transition: width 0.5s ease;
}

.card {
  background: #1e293b;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card h6 {
  color: #cbd5e1;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.2);
}

.card .card-body {
  color: #cbd5e1;
}

.card .card-body .text-secondary {
  color: #9ca3af;
}

.card .card-body .text-muted {
  color: #6b7280;
}

.card .card-body .btn {
  margin-bottom: 10px;
}

.card .card-body .list-group-item {
  background: #1e293b;
  border: none;
}

.card .card-body .list-group-item:hover {
  background: #334155;
}

.card .card-body .icon-inline {
  width: 24px;
  height: 24px;
  stroke-width: 2;
}

.card .card-body ul {
  list-style-type: none;
  padding: 0;
}

.card .card-body li {
  margin-bottom: 10px;
}

.card .card-body .list-unstyled {
  padding-left: 0;
}

.card .card-body .text-muted {
  color: #6b7280 !important;
}

.card .card-body .text-muted {
  color: #6b7280 !important;
}

.card h6 {
  color: #cbd5e1;
}


.skill-card {
  background: #1e293b;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.skill-card:hover {
  transform: scale(1.1);
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.2);
}

.skill-card i {
  transition: color 0.3s ease;
}

.skill-card:hover i {
  color: #01c879; /* Highlight color on hover */
}

.text-container {
  text-align: left; /* Rata kiri untuk teks */
  margin: 0 auto; /* Center secara horizontal dalam kontainer */
  max-width: 100%; /* Pastikan lebar maksimal 100% dari kontainer */
  padding: 0 15px; /* Ruang tambahan di kiri dan kanan */
}

.text-muted {
  color: #6b7280;
}

.mt-2 {
  margin-top: 0.5rem;
}

/* Responsif */
@media (max-width: 767px) {
  .text-container {
    padding-left: 10px;
    padding-right: 10px;
  }
}

</style>