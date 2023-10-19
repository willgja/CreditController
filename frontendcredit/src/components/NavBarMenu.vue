<template>
    <nav class="navbar">
      <div class="navbar-container">
        <!-- Logo e links da Navbar -->
        <div class="navbar-logo">Logo</div>
        <div class="navbar-links">
          <a href="#">Início</a>
          <a href="#">Pesquisa</a>
          <a href="#">Imagens</a>
          <a href="#">Maps</a>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'NavBarMenu',
  };
  </script>
  
  <style scoped>
  /* Estilos para a Navbar */
  .navbar {
    background-color: #4285f4; /* Cor de fundo azul semelhante ao Google */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Sombra */
    border-radius: 12px; /* Bordas arredondadas */
    padding: 10px 0;
    position: fixed; /* Fixar a Navbar no topo */
    top: 0; /* Alinhar ao topo da página */
    width: calc(100% - 20px); /* Largura total da tela */
    overflow: hidden; /* Evitar que o conteúdo se sobreponha */
    margin: 5px;
  }
  
  .navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
  }
  
  .navbar-logo {
    font-size: 24px;
    color: white;
    font-weight: bold;
    text-decoration: none;
  }
  
  .navbar-links {
    display: flex;
  }
  
  .navbar-links a {
    color: white;
    text-decoration: none;
    margin-right: 15px;
  }
  
  .navbar-links a:hover {
    text-decoration: underline;
  }


  </style>
  