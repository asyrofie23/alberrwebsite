<template>
    <section id="services" class="services">
      <div class="container">
        <h2>Layanan Kami</h2>
        <div class="services-grid">
          <div class="service-card" v-for="(service, index) in services" :key="index">
            <div class="service-icon">
              <i :class="service.icon"></i>
            </div>
            <h3>{{ service.title }}</h3>
            <p>{{ service.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ServicesSection',
    data() {
      return {
        services: [
          {
            icon: 'fas fa-graduation-cap',
            title: 'Program Pendidikan',
            description: 'Program pendidikan berkualitas untuk semua usia'
          },
          {
            icon: 'fas fa-users',
            title: 'Pelatihan',
            description: 'Pelatihan profesional untuk meningkatkan keterampilan'
          },
          {
            icon: 'fas fa-hand-holding-heart',
            title: 'Layanan Sosial',
            description: 'Bantuan sosial untuk masyarakat membutuhkan'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .services {
    text-align: center;
  }
  
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    margin-top: 40px;
  }
  
  .service-card {
    background: white;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s;
  }
  
  .service-card:hover {
    transform: translateY(-10px);
  }
  
  .service-icon {
    font-size: 2.5rem;
    color: #42b983;
    margin-bottom: 20px;
  }
  
  .service-card h3 {
    margin-bottom: 15px;
  }
  </style>