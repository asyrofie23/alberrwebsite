<template>
    <section id="contact" class="contact">
      <div class="container">
        <h2>Hubungi Kami</h2>
        <div class="contact-content">
          <div class="contact-info">
            <h3>Informasi Kontak</h3>
            <p><i class="fas fa-map-marker-alt"></i> Alamat: Jl. Contoh No. 123, Kota</p>
            <p><i class="fas fa-phone"></i> Telepon: (021) 123-4567</p>
            <p><i class="fas fa-envelope"></i> Email: info@lembaga.com</p>
          </div>
          <form class="contact-form" @submit.prevent="submitForm">
            <div class="form-group">
              <input type="text" v-model="form.name" placeholder="Nama Anda" required>
            </div>
            <div class="form-group">
              <input type="email" v-model="form.email" placeholder="Email Anda" required>
            </div>
            <div class="form-group">
              <textarea v-model="form.message" placeholder="Pesan Anda" required></textarea>
            </div>
            <button type="submit" class="submit-button">Kirim Pesan</button>
          </form>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ContactSection',
    data() {
      return {
        form: {
          name: '',
          email: '',
          message: ''
        }
      }
    },
    methods: {
      submitForm() {
        // Logika untuk mengirim form
        alert(`Terima kasih ${this.form.name}, pesan Anda telah terkirim!`);
        this.form = {
          name: '',
          email: '',
          message: ''
        };
      }
    }
  }
  </script>
  
  <style scoped>
  .contact {
    background-color: #f9f9f9;
  }
  
  .contact-content {
    display: flex;
    gap: 40px;
    margin-top: 30px;
  }
  
  .contact-info, .contact-form {
    flex: 1;
  }
  
  .contact-info p {
    margin-bottom: 15px;
    display: flex;
    align-items: center;
  }
  
  .contact-info i {
    margin-right: 10px;
    color: #42b983;
    width: 20px;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  .form-group input,
  .form-group textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-family: inherit;
  }
  
  .form-group textarea {
    height: 150px;
    resize: vertical;
  }
  
  .submit-button {
    background-color: #42b983;
    color: white;
    border: none;
    padding: 12px 30px;
    font-size: 1rem;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .submit-button:hover {
    background-color: #369f6b;
  }
  
  @media (max-width: 768px) {
    .contact-content {
      flex-direction: column;
    }
  }
  </style>