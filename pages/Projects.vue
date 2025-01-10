<template>
  <div>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <Navbar />
    <section class="projects">
      <div class="container">
        <h2 class="text-center mb-5">My Projects</h2>
        <div class="row">
          <div v-for="project in projects" :key="project.id" class="col-md-4 mb-4">
            <div class="card project-card">
              <img :src="project.image" class="card-img-top" :alt="project.title">
              <div class="card-body">
                <h5 class="card-title">{{ project.title }}</h5>
                <p class="card-text">
                  {{ truncateText(project.description) }}
                </p>
                <div class="d-flex justify-content-between">
                  <a :href="project.link" class="btn btn-primary" target="_blank">View Project</a>
                  <button class="btn btn-outline-light" @click="showDetails(project)">View Details</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <Footer />

    <!-- Modal -->
    <div v-if="selectedProject" class="modal fade show" tabindex="-1" style="display: block; background: rgba(0,0,0,0.5);">
      <div class="modal-dialog modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">{{ selectedProject.title }}</h5>
            <button type="button" class="close" @click="closeModal">&times;</button>
          </div>
          <div class="modal-body modal-scrollable">
            <img :src="selectedProject.image" class="img-fluid mb-3" :alt="selectedProject.title">
            <p class="project-description">{{ selectedProject.description }}</p>
          </div>
          <div class="modal-footer">
            <a :href="selectedProject.link" class="btn btn-primary" target="_blank">Visit Project</a>
            <button type="button" class="btn btn-secondary" @click="closeModal">Close</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
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
      projects: [
        {
          id: 1,
          title: 'NusAIra',
          description: 'NusAIra adalah platform berbasis teknologi yang dirancang untuk memberdayakan petambak lele melalui integrasi kecerdasan buatan, analitik data, dan manajemen tambak modern. Produk ini menawarkan berbagai fitur utama yang berdampak langsung pada efisiensi dan produktivitas petambak.Fitur Prediksi Harga Lele menggunakan teknologi AI untuk memberikan informasi real-time mengenai fluktuasi harga pasar, membantu petambak merencanakan penjualan secara strategis. NusAIra juga dilengkapi dengan Fitur Chatbot yang responsif, memberikan panduan instan tentang manajemen tambak, pemeliharaan lele, dan solusi teknis lainnya. Dashboard Manajemen Tambak memungkinkan petambak memonitor data operasional tambak secara real-time, seperti kualitas air dan penggunaan pakan, sehingga pengelolaan tambak menjadi lebih efektif. Selain itu, Perpustakaan Digital NusAIra menyediakan akses ke berbagai sumber edukasi, panduan, dan artikel untuk meningkatkan pengetahuan dan keterampilan petambak dalam budidaya lele yang modern dan berkelanjutan.Melalui kombinasi fitur-fitur inovatif ini, dampaknya, petambak lele dapat membuat keputusan bisnis yang lebih cerdas, meningkatkan hasil panen, dan berkontribusi pada keberlanjutan sektor perikanan Indonesia. NusAIra bukan hanya alat teknologi; ini adalah mitra strategis untuk keberhasilan usaha tambak lele Anda.',
          image: P1Image,
          link: 'https://nusaira.vercel.app/'
        },
        {
          id: 2,
          title: 'TOP-UP IN',
          description:  'TOP-UP IN adalah platform berbasis web yang dirancang untuk mempermudah berbagai transaksi pembayaran dan pembelian secara online. Dengan dukungan teknologi modern seperti Vue.js, Vite, Swiper, Bootstrap, dan FontAwesome, TOP-UP IN menghadirkan antarmuka pengguna yang responsif, interaktif, dan user-friendly.Platform ini dirancang untuk memberikan pengalaman bertransaksi yang nyaman dan efisien, serta memastikan setiap fitur bekerja secara optimal di berbagai perangkat.',
          image: P2Image,
          link: 'https://github.com/praditus343/SiPPOB-UAS'
        },
        {
          id: 3,
          title: 'Big data & Predictive Analytics Final project Harga saham PT Telekomunikasi Indonesia Tbk (TLKM)',
          description: 'Proyek ini bertujuan untuk menganalisis harga saham PT Telekomunikasi Indonesia Tbk(TLKM) menggunakan teknik Big Data dan Predictive Analytics. Dengan memanfaatkan data historis harga saham, volume perdagangan, dan faktor-faktor ekonomi makro, proyek ini mengembangkan model prediksi yang dapat membantu investor dalam membuat keputusan investasi yang lebih informatif. Analisis ini melibatkan pengumpulan dan pemrosesan data besar dari berbagai sumber, termasuk data pasar saham dan indikator ekonomi. Metode analisis yang digunakan mencakup teknik statistik dan machine learning untuk mengidentifikasi pola dan tren dalam pergerakan harga saham TLKM. Hasil dari proyek ini diharapkan dapat memberikan wawasan yang lebih mendalam mengenai dinamika harga saham TLKM, serta faktor-faktor yang mempengaruhi pergerakannya. Dengan demikian, investor dapat membuat keputusan investasi yang lebih tepat dan strategis berdasarkan analisis yang komprehensif.',
          image: P3Image,
          link: 'https://colab.research.google.com/drive/1fti1OhKwyro_eFDNFv6ZRynCzt3jCExq#scrollTo=lGVGfJS6z2lA'
        },
        {
          id: 4,
          title: 'HEART SYNC - Smart Watch Application',
          description: 'HEART SYNC adalah aplikasi smartwatch yang dirancang untuk memantau dan menganalisis data detak jantung pengguna secara real-time. Aplikasi ini memanfaatkan teknologi sensor detak jantung yang terintegrasi pada smartwatch untuk mengukur dan merekam data detak jantung pengguna. Data tersebut kemudian diproses dan dianalisis menggunakan algoritma machine learning untuk mendeteksi pola dan anomali detak jantung yang mungkin terjadi. Aplikasi ini juga dilengkapi dengan fitur notifikasi yang memberitahukan pengguna jika terdeteksi adanya perubahan signifikan dalam detak jantungnya, sehingga pengguna dapat segera mengambil tindakan yang diperlukan. HEART SYNC dirancang dengan antarmuka yang sederhana dan intuitif, memastikan pengguna dapat dengan mudah mengakses dan memahami data detak jantung mereka. Aplikasi ini juga menyediakan riwayat data detak jantung yang tercatat, sehingga pengguna dapat melacak perkembangan detak jantung mereka dari waktu ke waktu. Dengan HEART SYNC, pengguna dapat memantau kesehatan jantung mereka secara real-time dan proaktif, sehingga dapat mencegah risiko penyakit jantung dan menjaga kesehatan jantung mereka dengan lebih baik.',
          image: P4Image,
          link: 'https://praditus343.github.io/IMK/'
        },
        {
          id: 5,
          title: 'HitungLuas',
          description: '"HitungLuas" adalah aplikasi web interaktif yang membantu pengguna menghitung luas berbagai bentuk geometri dua dimensi, seperti persegi, persegi panjang, segitiga, dan lingkaran. Aplikasi ini dirancang dengan antarmuka yang sederhana dan intuitif, memudahkan pengguna dalam memasukkan parameter yang diperlukan dan mendapatkan hasil perhitungan secara instan.Aplikasi ini dibangun menggunakan HTML, CSS, dan JavaScript, dengan desain responsif yang memastikan tampilan optimal di berbagai perangkat. Kode sumber lengkap dan dokumentasi proyek tersedia di repository GitHub berikut: https://github.com/praditus343/Perhitungan-Luas-Bangun-Datar',
          image: P5Image,
          link: 'https://praditus343.github.io/Perhitungan-Luas-Bangun-Datar/'
        },
        {
          id: 6,
          title: 'LogicGateHub',
          description: 'LogicGateHub adalah simulator gerbang logika digital yang dirancang untuk membantu mahasiswa dan profesional dalam memahami dan menguji fungsi gerbang logika dasar. Aplikasi ini menyediakan antarmuka interaktif yang memungkinkan pengguna untuk membuat rangkaian logika dengan menambahkan gerbang logika, input, dan output sesuai kebutuhan. Pengguna dapat mengatur nilai input dan melihat hasil keluaran dari rangkaian logika yang dibuat. LogicGateHub juga dilengkapi dengan fitur simulasi real-time yang memungkinkan pengguna untuk melihat perubahan output saat nilai input diubah. Aplikasi ini dirancang dengan desain yang sederhana dan intuitif, memastikan pengguna dapat dengan mudah mengoperasikannya tanpa memerlukan pengetahuan teknis yang mendalam. Dengan LogicGateHub, pengguna dapat belajar dan menguji gerbang logika digital dengan cara yang interaktif dan menyenangkan.',
          image: P6Image,
          link: 'https://praditus343.github.io/Simulator-Gerbang-Logika/'
        },
      ]
    };
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
    }
  }
};
</script>

<style scoped>
.projects {
  padding: 80px 0;
  background: #0f172a;
  color: #fff;
}

.projects h2 {
  color: #cbd5e1;
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 30px; /* Menambahkan margin bottom agar lebih rapi */
  text-align: center;
}

.project-card {
  background: #1e293b;
  border-radius: 15px;
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s;
  height: 100%; /* Pastikan card mengisi ruang yang ada */
}

.project-card:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
}

.project-card .card-img-top {
  height: 200px;
  object-fit: cover;
  border-bottom: 2px solid #2d3748; /* Menambahkan border di bawah gambar untuk konsistensi */
}

.project-card .card-body {
  padding: 15px; /* Menambahkan padding agar lebih rapi */
  color: #cbd5e1;
}

.project-card .card-title {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 15px; /* Memberikan jarak antara judul dan deskripsi */
  color: #fff;
}

.project-card .card-text {
  font-size: 0.875rem;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}

.project-card .d-flex {
  justify-content: space-between;
}

.btn-primary {
  background-color: #01c879;
  border-color: #01c879;
  padding: 5px 15px;
}

.btn-primary:hover {
  background-color: #019d6b;
  border-color: #019d6b;
}

.btn-outline-light {
  color: #fff;
  border-color: #fff;
}

.btn-outline-light:hover {
  background-color: #fff;
  color: #1e293b;
}

.modal-content {
  background: #1e293b;
  color: #fff;
}

.modal-header, .modal-footer {
  border-color: #2d3748;
}

.modal-title {
  color: #cbd5e1;
  font-size: 1.5rem;
}

.modal-body {
  padding: 20px;
}

.modal-scrollable {
  max-height: 500px;
  overflow-y: auto;
  padding-right: 10px;
}

.project-description {
  white-space: pre-wrap;
  word-wrap: break-word;
  line-height: 1.5;
  padding: 10px;
  color: #cbd5e1;
  text-align: justify;
}

/* Hide scrollbar */
.modal-scrollable::-webkit-scrollbar {
  width: 0;
}
</style>
