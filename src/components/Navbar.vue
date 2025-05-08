<template>
    <nav class="navbar">
      <div class="container">
        <div class="navbar-brand">
          <router-link to="/" class="logo">PONDOK PESANTREN ALBERR</router-link>
        </div>
        <ul class="navbar-menu">
          <li><router-link to="/">Beranda</router-link></li>
          <li><router-link to="/about">Tentang</router-link></li>
          <li><router-link to="/services">Layanan</router-link></li>
          <li><router-link to="/contact">Kontak</router-link></li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar'
  }
  </script>
  
  <style scoped>
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
  }
  
  .navbar-menu {
    display: flex;
    list-style: none;
  }
  
  .navbar-menu li {
    margin-left: 20px;
  }
  
  .navbar-menu a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .navbar-menu a:hover {
    color: #42b983;
  }
  </style>