<template>
    <section class="hero">
      <div class="container">
        <h1>Selamat Datang di Nama Lembaga</h1>
        <p>Lembaga profesional yang berkomitmen untuk memberikan pelayanan terbaik</p>
        <button class="cta-button">Pelajari Lebih Lanjut</button>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'HeroSection'
  }
  </script>
  
  <style scoped>
  .hero {
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), 
                url('https://via.placeholder.com/1920x1080') no-repeat center center/cover;
    color: white;
    text-align: center;
    padding: 150px 0;
    margin-top: 60px; /* Untuk mengkompensasi navbar fixed */
  }
  
  .hero h1 {
    font-size: 3rem;
    margin-bottom: 20px;
  }
  
  .hero p {
    font-size: 1.5rem;
    margin-bottom: 30px;
  }
  
  .cta-button {
    background-color: #42b983;
    color: white;
    border: none;
    padding: 12px 30px;
    font-size: 1.2rem;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .cta-button:hover {
    background-color: #369f6b;
  }
  </style>