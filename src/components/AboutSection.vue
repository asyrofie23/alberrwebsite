<template>
    <section id="about" class="about">
      <div class="container">
        <h2>Tentang Kami</h2>
        <div class="about-content">
          <div class="about-text">
            <p>Nama Lembaga adalah lembaga yang berdiri sejak tahun 20XX dengan visi untuk memberikan pelayanan terbaik di bidang pendidikan/kesehatan/sosial (sesuaikan).</p>
            <p>Kami memiliki tim profesional yang siap membantu Anda mencapai tujuan Anda.</p>
          </div>
          <div class="about-image">
            <img src="https://via.placeholder.com/500x300" alt="Tentang Kami">
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'AboutSection'
  }
  </script>
  
  <style scoped>
  .about {
    background-color: #f9f9f9;
  }
  
  .about-content {
    display: flex;
    align-items: center;
    gap: 40px;
    margin-top: 30px;
  }
  
  .about-text {
    flex: 1;
  }
  
  .about-image {
    flex: 1;
  }
  
  .about-image img {
    width: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  @media (max-width: 768px) {
    .about-content {
      flex-direction: column;
    }
  }
  </style>