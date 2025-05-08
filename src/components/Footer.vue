<template>
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-section">
            <h3>Tentang Lembaga</h3>
            <p>Lembaga profesional yang berkomitmen untuk memberikan pelayanan terbaik di bidang pendidikan/kesehatan/sosial.</p>
          </div>
          <div class="footer-section">
            <h3>Link Cepat</h3>
            <ul>
              <li><router-link to="/">Beranda</router-link></li>
              <li><router-link to="/about">Tentang</router-link></li>
              <li><router-link to="/services">Layanan</router-link></li>
              <li><router-link to="/contact">Kontak</router-link></li>
            </ul>
          </div>
          <div class="footer-section">
            <h3>Kontak</h3>
            <p><i class="fas fa-map-marker-alt"></i> Jl. Contoh No. 123, Kota</p>
            <p><i class="fas fa-phone"></i> (021) 123-4567</p>
            <p><i class="fas fa-envelope"></i> info@lembaga.com</p>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; {{ currentYear }} Nama Lembaga. Semua Hak Dilindungi.</p>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
    data() {
      return {
        currentYear: new Date().getFullYear()
      }
    }
  }
  </script>
  
  <style scoped>
  .footer {
    background-color: #2c3e50;
    color: white;
    padding: 60px 0 20px;
  }
  
  .footer-content {
    display: flex;
    justify-content: space-between;
    margin-bottom: 40px;
  }
  
  .footer-section {
    flex: 1;
    padding: 0 20px;
  }
  
  .footer-section h3 {
    margin-bottom: 20px;
    font-size: 1.2rem;
  }
  
  .footer-section p, .footer-section li {
    margin-bottom: 10px;
    color: #ecf0f1;
  }
  
  .footer-section a {
    color: #ecf0f1;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .footer-section a:hover {
    color: #42b983;
  }
  
  .footer-section i {
    margin-right: 10px;
    color: #42b983;
  }
  
  .footer-bottom {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid #34495e;
    color: #ecf0f1;
    font-size: 0.9rem;
  }
  
  @media (max-width: 768px) {
    .footer-content {
      flex-direction: column;
      gap: 30px;
    }
    
    .footer-section {
      padding: 0;
    }
  }
  </style>