<template>
  <div>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <Navbar />
    <section class="projects">
      <div class="container">
        <h2 class="text-center mb-5" data-aos="fade-down">My Projects</h2>
        <!-- Filter Buttons -->
        <div class="filter-buttons mb-4" data-aos="fade-up">
          <button 
            v-for="category in categories" 
            :key="category"
            @click="filterProjects(category)"
            :class="['filter-btn', { active: currentCategory === category }]"
          >
            {{ category }}
          </button>
        </div>
        <div class="row">
          <div 
            v-for="project in filteredProjects" 
            :key="project.id" 
            class="col-md-4 mb-4"
            data-aos="fade-up"
            :data-aos-delay="project.id * 100"
          >
            <div class="card project-card">
              <div class="project-image-container">
                <img :src="project.image" class="card-img-top" :alt="project.title">
                <div class="project-overlay">
                  <div class="project-tech">
                    <span v-for="tech in project.technologies" :key="tech" class="tech-badge">
                      {{ tech }}
                    </span>
                  </div>
                </div>
              </div>
              <div class="card-body">
                <h5 class="card-title" style="white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">{{ project.title }}</h5>
                <p class="card-text" style="display: -webkit-box; -webkit-box-orient: vertical; -webkit-line-clamp: 3; overflow: hidden;">
                  {{ truncateText(project.description) }}
                </p>
                  <div class="project-links d-flex justify-content-between">
                    <a :href="project.link" class="btn btn-primary" target="_blank">
                      <i class="fas fa-external-link-alt mr-2"></i>View Project
                    </a>
                    <button class="btn btn-outline-light" @click="showDetails(project)">
                      <i class="fas fa-info-circle mr-2"></i>Details
                    </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <Footer />

    <!-- Modal -->
    <div v-if="selectedProject" class="modal fade show" tabindex="-1" style="display: block; background: rgba(0,0,0,0.8);">
      <div class="modal-dialog modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">{{ selectedProject.title }}</h5>
            <button type="button" class="close" @click="closeModal">&times;</button>
          </div>
          <div class="modal-body modal-scrollable">
            <div class="project-gallery mb-4">
              <img :src="selectedProject.image" class="img-fluid" :alt="selectedProject.title">
            </div>
            <div class="project-details">
              <h6 class="details-title">Technologies Used:</h6>
              <div class="tech-stack mb-3">
                <span v-for="tech in selectedProject.technologies" :key="tech" class="tech-badge">
                  {{ tech }}
                </span>
              </div>
              <h6 class="details-title">Project Description:</h6>
              <p class="project-description">{{ selectedProject.description }}</p>
              <h6 class="details-title">Key Features:</h6>
              <ul class="feature-list">
                <li v-for="feature in selectedProject.features" :key="feature">{{ feature }}</li>
              </ul>
            </div>
          </div>
          <div class="modal-footer">
            <a :href="selectedProject.link" class="btn btn-primary" target="_blank">
              <i class="fas fa-external-link-alt mr-2"></i>Visit Project
            </a>
            <button type="button" class="btn btn-secondary" @click="closeModal">Close</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
import P1Image from "../assets/img/P1.jpeg";
import P2Image from "../assets/img/P2.png";
import P3Image from "../assets/img/P3.png";
import P4Image from "../assets/img/P4.png";
import P5Image from "../assets/img/P5.png";
import P6Image from "../assets/img/P6.png";

export default {
  name: 'Projects',
  data() {
    return {
      selectedProject: null,
      currentCategory: 'All',
      categories: ['All', 'Web Development', 'Data Science', 'UI/UX Design'],
      projects: [
        {
          id: 1,
          title: 'NusAIra',
          description: 'NusAIra adalah platform berbasis teknologi yang dirancang untuk memberdayakan petambak lele melalui integrasi kecerdasan buatan, analitik data, dan manajemen tambak modern. Produk ini menawarkan berbagai fitur utama yang berdampak langsung pada efisiensi dan produktivitas petambak.',
          image: P1Image,
          link: 'https://nusaira.vercel.app/',
          category: 'Web Development',
          technologies: ['Vue.js', 'Node.js', 'AI/ML', 'Bootstrap'],
          features: [
            'Prediksi Harga Lele menggunakan AI',
            'Chatbot Responsif untuk Panduan',
            'Dashboard Manajemen Tambak Real-time',
            'Perpustakaan Digital'
          ]
        },
        {
          id: 2,
          title: 'TOP-UP IN',
          description: 'TOP-UP IN adalah platform berbasis web yang dirancang untuk mempermudah berbagai transaksi pembayaran dan pembelian secara online. Dengan dukungan teknologi modern seperti Vue.js, Vite, Swiper, Bootstrap, dan FontAwesome, TOP-UP IN menghadirkan antarmuka pengguna yang responsif, interaktif, dan user-friendly.',
          image: P2Image,
          link: 'https://github.com/praditus343/SiPPOB-UAS',
          category: 'Web Development',
          technologies: ['Vue.js', 'Vite', 'Bootstrap', 'Swiper'],
          features: [
            'Sistem Pembayaran Online',
            'Interface Responsif',
            'Manajemen Transaksi',
            'Riwayat Pembayaran'
          ]
        },
        {
          id: 3,
          title: 'Big data & Predictive Analytics - TLKM Stock',
          description: 'Proyek ini bertujuan untuk menganalisis harga saham PT Telekomunikasi Indonesia Tbk(TLKM) menggunakan teknik Big Data dan Predictive Analytics.',
          image: P3Image,
          link: 'https://colab.research.google.com/drive/1fti1OhKwyro_eFDNFv6ZRynCzt3jCExq#scrollTo=lGVGfJS6z2lA',
          category: 'Data Science',
          technologies: ['Python', 'Pandas', 'Scikit-learn', 'Matplotlib'],
          features: [
            'Analisis Data Historis',
            'Prediksi Harga Saham',
            'Visualisasi Data',
            'Machine Learning Models'
          ]
        },
        {
          id: 4,
          title: 'HEART SYNC - Smart Watch Application',
          description: 'HEART SYNC adalah aplikasi smartwatch yang dirancang untuk memantau dan menganalisis data detak jantung pengguna secara real-time.',
          image: P4Image,
          link: 'https://praditus343.github.io/IMK/',
          category: 'UI/UX Design',
          technologies: ['Figma', 'Adobe XD', 'Prototyping', 'UI Design'],
          features: [
            'Real-time Heart Rate Monitoring',
            'Health Analytics Dashboard',
            'Customizable Alerts',
            'Data Visualization'
          ]
        },
        {
          id: 5,
          title: 'HitungLuas',
          description: 'HitungLuas adalah aplikasi web interaktif yang membantu pengguna menghitung luas berbagai bentuk geometri dua dimensi.',
          image: P5Image,
          link: 'https://praditus343.github.io/Perhitungan-Luas-Bangun-Datar/',
          category: 'Web Development',
          technologies: ['HTML', 'CSS', 'JavaScript', 'Bootstrap'],
          features: [
            'Kalkulator Geometri',
            'Interface Intuitif',
            'Multiple Shape Support',
            'Responsive Design'
          ]
        },
        {
          id: 6,
          title: 'LogicGateHub',
          description: 'LogicGateHub adalah simulator gerbang logika digital yang dirancang untuk membantu mahasiswa dan profesional dalam memahami dan menguji fungsi gerbang logika dasar.',
          image: P6Image,
          link: 'https://praditus343.github.io/Simulator-Gerbang-Logika/',
          category: 'Web Development',
          technologies: ['JavaScript', 'HTML Canvas', 'CSS', 'SVG'],
          features: [
            'Interactive Logic Gates',
            'Real-time Simulation',
            'Circuit Building',
            'Truth Table Generator'
          ]
        },
      ]
    };
  },
  computed: {
    filteredProjects() {
      if (this.currentCategory === 'All') {
        return this.projects;
      }
      return this.projects.filter(project => project.category === this.currentCategory);
    }
  },
  methods: {
    truncateText(text, maxLength = 100) {
      return text.length > maxLength ? text.substring(0, maxLength) + '...' : text;
    },
    showDetails(project) {
      this.selectedProject = project;
    },
    closeModal() {
      this.selectedProject = null;
    },
    filterProjects(category) {
      this.currentCategory = category;
    }
  },
  mounted() {
    if (typeof AOS !== 'undefined') {
      AOS.init({
        duration: 800,
        once: true,
        offset: 100
      });
    }
  }
};
</script>

<style scoped>
.projects {
  padding: 80px 0;
  background: #0f172a;
  color: #fff;
  min-height: 100vh;
}

.projects h2 {
  color: #cbd5e1;
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 40px;
  position: relative;
  display: inline-block;
}

.projects h2::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 3px;
  background: #01c879;
}

.filter-buttons {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  margin-bottom: 30px;
}

.filter-btn {
  background: transparent;
  border: 2px solid #01c879;
  color: #cbd5e1;
  padding: 8px 20px;
  border-radius: 25px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.filter-btn:hover, .filter-btn.active {
  background: #01c879;
  color: #fff;
}

.project-card {
  background: #1e293b;
  border-radius: 15px;
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s;
  height: 100%;
  border: none;
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.4);
}

.project-image-container {
  position: relative;
  overflow: hidden;
}

.project-card .card-img-top {
  height: 200px;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.project-card:hover .card-img-top {
  transform: scale(1.1);
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(1, 200, 121, 0.9);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-tech {
  padding: 15px;
  text-align: center;
}

.tech-badge {
  display: inline-block;
  background: rgba(255, 255, 255, 0.9);
  color: #1e293b;
  padding: 5px 10px;
  border-radius: 15px;
  font-size: 0.8rem;
  margin: 3px;
  font-weight: 500;
}

.project-card .card-body {
  padding: 20px;
  color: #cbd5e1;
}

.project-card .card-title {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 15px;
  color: #fff;
}

.project-card .card-text {
  font-size: 0.9rem;
  line-height: 1.6;
  margin-bottom: 20px;
}

.project-links {
  display: flex;
  gap: 10px;
}

.btn-primary {
  background-color: #01c879;
  border-color: #01c879;
  padding: 8px 15px;
  border-radius: 20px;
  font-size: 0.9rem;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  background-color: #019d6b;
  border-color: #019d6b;
  transform: translateY(-2px);
}

.btn-outline-light {
  color: #cbd5e1;
  border-color: #cbd5e1;
  padding: 8px 15px;
  border-radius: 20px;
  font-size: 0.9rem;
  transition: all 0.3s ease;
}

.btn-outline-light:hover {
  background-color: #cbd5e1;
  color: #1e293b;
  transform: translateY(-2px);
}

.modal-content {
  background: #1e293b;
  color: #fff;
  border-radius: 15px;
}

.modal-header {
  border-bottom: 1px solid #2d3748;
  padding: 20px;
}

.modal-title {
  color: #cbd5e1;
  font-size: 1.5rem;
  font-weight: 600;
}

.modal-body {
  padding: 25px;
}

.modal-scrollable {
  max-height: 70vh;
  overflow-y: auto;
}

.project-gallery {
  border-radius: 10px;
  overflow: hidden;
  margin-bottom: 25px;
}

.project-gallery img {
  width: 100%;
  border-radius: 10px;
}

.details-title {
  color: #01c879;
  font-size: 1.1rem;
  margin-bottom: 10px;
  font-weight: 600;
}

.tech-stack {
  margin-bottom: 20px;
}

.feature-list {
  list-style-type: none;
  padding-left: 0;
}

.feature-list li {
  position: relative;
  padding-left: 25px;
  margin-bottom: 10px;
  color: #cbd5e1;
}

.feature-list li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: #01c879;
}

.modal-footer {
  border-top: 1px solid #2d3748;
  padding: 20px;
}

.btn-secondary {
  background-color: #4b5563;
  border-color: #4b5563;
  transition: all 0.3s ease;
}

.btn-secondary:hover {
  background-color: #374151;
  border-color: #374151;
}

@media (max-width: 768px) {
  .projects {
    padding: 50px 0;
  }

  .projects h2 {
    font-size: 2rem;
  }

  .filter-buttons {
    gap: 10px;
  }

  .filter-btn {
    padding: 6px 15px;
    font-size: 0.9rem;
  }

  .project-card .card-img-top {
    height: 180px;
  }

  .project-links {
    flex-direction: column;
  }

  .modal-dialog {
    margin: 10px;
  }
}
</style>
