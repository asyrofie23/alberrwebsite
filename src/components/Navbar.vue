<template>
    <nav class="navbar">
      <div class="container">
        <div class="navbar-brand">
          <router-link to="/" class="logo">
            <img src="@/assets/logo.png" alt="Logo Pondok Pesantren Alberr" class="logo-image">
            PONDOK PESANTREN ALBERR
          </router-link>
        </div>
        <ul class="navbar-menu">
          <li class="dropdown" 
              @mouseenter="openDropdown('beranda')" 
              @mouseleave="closeDropdown('beranda')">
            <router-link to="/">Beranda <i class="fas fa-chevron-down"></i></router-link>
            <ul class="dropdown-menu" v-show="activeDropdown === 'beranda'" transition="fade">
              <li><router-link to="/beranda/profil">Profil Singkat</router-link></li>
              <li><router-link to="/beranda/berita">Berita Terkini</router-link></li>
              <li><router-link to="/beranda/galeri">Galeri</router-link></li>
            </ul>
          </li>
          
          <li class="dropdown" 
              @mouseenter="openDropdown('tentang')" 
              @mouseleave="closeDropdown('tentang')">
            <router-link to="/about">Tentang <i class="fas fa-chevron-down"></i></router-link>
            <ul class="dropdown-menu" v-show="activeDropdown === 'tentang'" transition="fade">
              <li><router-link to="/about/sejarah">Sejarah</router-link></li>
              <li><router-link to="/about/visi-misi">Visi & Misi</router-link></li>
              <li><router-link to="/about/pengasuh">Pengasuh</router-link></li>
            </ul>
          </li>
          
          <li class="dropdown" 
              @mouseenter="openDropdown('layanan')" 
              @mouseleave="closeDropdown('layanan')">
            <router-link to="/services">Layanan <i class="fas fa-chevron-down"></i></router-link>
            <ul class="dropdown-menu" v-show="activeDropdown === 'layanan'" transition="fade">
              <li><router-link to="/services/pmb">Penerimaan Murid Baru</router-link></li>
              <li><router-link to="/services/tahfidz">Program Tahfidz</router-link></li>
              <li><router-link to="/services/kegiatan">Kegiatan Santri</router-link></li>
            </ul>
          </li>
          
          <li class="dropdown" 
              @mouseenter="openDropdown('kontak')" 
              @mouseleave="closeDropdown('kontak')">
            <router-link to="/contact">Kontak <i class="fas fa-chevron-down"></i></router-link>
            <ul class="dropdown-menu" v-show="activeDropdown === 'kontak'" transition="fade">
              <li><router-link to="/contact/lokasi">Lokasi</router-link></li>
              <li><router-link to="/contact/sosmed">Media Sosial</router-link></li>
              <li><router-link to="/contact/form">Form Kontak</router-link></li>
            </ul>
          </li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar',
    data() {
      return {
        activeDropdown: null
      }
    },
    methods: {
      openDropdown(menu) {
        this.activeDropdown = menu;
      },
      closeDropdown(menu) {
        if (this.activeDropdown === menu) {
          this.activeDropdown = null;
        }
      }
    }
  }
  </script>
  
  <style scoped>
  /* Gaya dasar navbar (sama seperti sebelumnya) */
  .navbar {
    background-color: #2c3e50;
    color: white;
    padding: 15px 0;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
  }
  
  .navbar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo {
    color: white;
    font-size: 1.5rem;
    font-weight: bold;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  
  .logo-image {
    height: 40px;
    width: auto;
  }
  
  .navbar-menu {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
  }
  
  .navbar-menu > li {
    position: relative;
    margin-left: 20px;
  }
  
  .navbar-menu a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
    padding: 10px 15px;
    display: flex;
    align-items: center;
    gap: 5px;
  }
  
  .navbar-menu a:hover {
    color: #42b983;
  }
  
  /* Gaya dropdown */
  .dropdown-menu {
    display: none;
    position: absolute;
    left: 0;
    top: 100%;
    color: #2c3e50;
    text-align: center;
    background-color: white;
    min-width: 200px;
    box-shadow: 0 8px 16px rgba(0,0,0,0.1);
    border-radius: 4px;
    list-style: none;
    padding: 10px 0;
    margin: 0;
    z-index: 1001;
  }
  
  .dropdown-menu a {
    color: #2c3e50 !important;
    padding: 8px 20px;
  }
  
  .dropdown-menu a:hover {
    color: #42b983 !important;
    background-color: #f8f9fa;
  }
  
  .dropdown:hover .dropdown-menu {
    display: block;
  }
  
  .dropdown-toggle .fa-chevron-down {
    font-size: 0.8rem;
    transition: transform 0.3s;
  }
  
  .dropdown:hover .dropdown-toggle .fa-chevron-down {
    transform: rotate(180deg);
  }
  
  /* Responsive Design */
  @media (max-width: 992px) {
    .navbar-menu {
      flex-direction: column;
      position: fixed;
      top: 70px;
      left: -100%;
      width: 80%;
      height: calc(100vh - 70px);
      background-color: #2c3e50;
      transition: left 0.3s;
      padding-top: 20px;
    }
    
    .navbar-menu.show {
      left: 0;
    }
    
    .navbar-menu > li {
      margin: 0;
    }
    
    .dropdown-menu {
      position: static;
      display: none;
      background-color: rgba(0,0,0,0.1);
      box-shadow: none;
    }
    
    .dropdown:hover .dropdown-menu {
      display: block;
    }
  }
  </style>