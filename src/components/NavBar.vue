<template>
    <nav class="translucent-navbar">
      <div class="nav-content">
        <a href="#" class="nav-link">Home</a>
        <a href="#" class="nav-link">About</a>
        <a href="#" class="nav-link">Services</a>
        <a href="#" class="nav-link">Contact</a>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'TranslucentNavbar',
  };
  </script>
  
  <style scoped>
  .translucent-navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: rgba(21,24,30, 0.2);
    backdrop-filter: blur(3px);
    -webkit-backdrop-filter: blur(3px);
    border-bottom: .5px solid rgba(255, 255, 255, 0.18);
    z-index: 999;
    color: var(--color-text);
    font-family: Inter, sans-serif;
    font-weight: 200;

  }
  
  .nav-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem;
    display: flex;
    justify-content: center;
  }
  
  .nav-link {
    color: white;
    text-decoration: none;
    margin: 0 10px;
  }
  </style>
  