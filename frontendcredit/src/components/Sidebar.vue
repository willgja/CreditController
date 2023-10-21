<template>
    <div class="sidebar" :class="{ 'sidebar-open': isSidebarOpen }">
      <div class="toggle-button" @click="toggleSidebar">
        <!-- Ícone do botão de alternância -->
      </div>
      <div class="user-profile">
        <!-- Foto do usuário logado -->
        <img src="user-avatar.jpg" alt="User Avatar" />
        <span>{{ userName }}</span>
      </div>
      <!-- Links do site, atalhos, etc. -->
      <ul class="sidebar-links">
        <li><a href="#">Início</a></li>
        <li><a href="#">Caixa de entrada</a></li>
        <!-- Outros links do site -->
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SideBar',
    data() {
      return {
        isSidebarOpen: true,
      };
    },
    methods: {
      toggleSidebar() {
        this.isSidebarOpen = !this.isSidebarOpen;
      },
    },
    computed: {
      userName() {
        // Lógica para obter o nome do usuário logado
        return "Nome do Usuário";
      },
    },
  };
  </script>
  
  <style scoped>
  /* Estilos para a Sidebar */
  .sidebar {
    width: 250px; /* Largura da sidebar quando aberta */
    height: 100%;
    background-color: #f2f2f2;
    position: fixed;
    top: 0;
    left: 0; /* Alterado para 0 quando aberto */
    transition: left 0.3s;
    overflow-y: auto;
    z-index: 100;
  }
  
  /* Quando a classe 'sidebar-open' não é aplicada, a sidebar fica fechada (left: -250px) */
  .sidebar:not(.sidebar-open) {
    left: -250px;
  }
  
  /* Estilos do botão de alternância (ícone) */
  .toggle-button {
    cursor: pointer;
    background-color: #4285f4;
    color: white;
    width: 60px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  /* Estilos da seção de perfil do usuário (foto e nome) */
  .user-profile {
    text-align: center;
    padding: 10px;
    /* Outros estilos da seção de perfil */
  }
  
  /* Estilos da lista de links da sidebar */
  .sidebar-links {
    list-style: none;
    padding: 0;
  }
  
  .sidebar-links li {
    padding: 10px;
    /* Estilos para cada item da lista de links */
  }
  </style>
  