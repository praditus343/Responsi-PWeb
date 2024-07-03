<template>
    <div>
      <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
      <Navbar />
    <section class="projects">
      <div class="container">
        <h2 class="text-center mb-5">My Projects</h2>
        <div class="row">
          <!-- Loop through projects array to display project items -->
          <div v-for="project in projects" :key="project.id" class="col-md-4 mb-4">
            <div class="card project-card">
              <img :src="project.image" class="card-img-top" :alt="project.title">
              <div class="card-body">
                <h5 class="card-title">{{ project.title }}</h5>
                <p class="card-text">{{ project.description }}</p>
                <a :href="project.link" class="btn btn-primary" target="_blank">View Project</a>
              </div>
              <div class="card-footer">
                <a :href="project.link" class="btn btn-outline-light" target="_blank">View Details</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <Footer />
    </div>
  </template>
  
  <script>
  export default {
    name: 'Projects',
    data() {
      return {
        // Sample data for projects
        projects: [
          {
            id: 1,
            title: 'Project One',
            description: 'A brief description of Project One.',
            image: '/assets/img/project1.png',
            link: 'https://example.com/project1'
          },
          {
            id: 2,
            title: 'Project Two',
            description: 'A brief description of Project Two.',
            image: '/assets/img/project2.png',
            link: 'https://example.com/project2'
          },
          {
            id: 3,
            title: 'Project Three',
            description: 'A brief description of Project Three.',
            image: '/assets/img/project3.png',
            link: 'https://example.com/project3'
          }
          // Add more projects as needed
        ]
      }
    }
  }
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
  }
  
  .project-card {
    background: #1e293b;
    border-radius: 15px;
    overflow: hidden;
    transition: all 0.3s ease;
    position: relative;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  }
  
  .project-card:hover {
    transform: scale(1.05);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
  }
  
  .project-card .card-img-top {
    height: 200px;
    object-fit: cover;
    transition: opacity 0.3s ease;
  }
  
  .project-card:hover .card-img-top {
    opacity: 0.8;
  }
  
  .project-card .card-body {
    color: #cbd5e1;
  }
  
  .project-card .card-title {
    font-size: 1.25rem;
    font-weight: 600;
    margin-bottom: 1rem;
  }
  
  .project-card .card-text {
    font-size: 0.875rem;
    color: #9ca3af;
    margin-bottom: 1.5rem;
  }
  
  .project-card .btn-primary {
    background-color: #01c879;
    border-color: #01c879;
  }
  
  .project-card .btn-primary:hover {
    background-color: #019d6b;
    border-color: #019d6b;
  }
  
  .project-card .card-footer {
    background: #1e293b;
    padding: 0.75rem;
    text-align: center;
  }
  
  .project-card .btn-outline-light {
    color: #fff;
    border-color: #fff;
  }
  
  .project-card .btn-outline-light:hover {
    background-color: #fff;
    color: #1e293b;
  }
  </style>
  