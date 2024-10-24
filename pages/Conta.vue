<template>
  <div>
    <div class="menu-bar">
      <div class="container">
        <img src="/logo.png" alt="Logo" class="logo" />
        <div class="search-container">
          <input type="text" placeholder="O que você está procurando?" class="search-input" />
        </div>
        <nav class="nav">
          <button class="nav-button">
            <img src="carrinho.png" alt="Carrinho" class="nav-icon" />
            <span class="nav-text">Carrinho</span>
          </button>
          <button class="nav-button">
            <img src="/favorite.png" alt="Favoritos" class="nav-icon" />
            <span class="nav-text">Favoritos</span>
          </button>
          <nuxt-link to="/Conta" class="nav-button"> <!-- Rota alterada para /Login -->
            <img src="/user.png" alt="Conta" class="nav-icon" />
            <span class="nav-text">Conta</span>
          </nuxt-link>
        </nav>
      </div>
    </div>
  
      <div class="content">
        <div class="login-container">
          <h2 class="login-title">Login</h2>
          <form @submit.prevent="handleLogin" class="login-form">
            <input type="email" v-model="email" placeholder="E-mail" class="input-field" required />
            <input type="password" v-model="password" placeholder="Senha" class="input-field" required />
            <button type="submit" class="login-button">Entrar</button>
            <p class="login-footer">
              Não tem uma conta? <router-link to="/register" class="register-link">Cadastre-se</router-link>
            </p>
          </form>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        password: ''
      };
    },
    methods: {
      handleLogin() {
        console.log('Login:', this.email, this.password);
      }
    }
  };
  </script>
  
  <style scoped>
  .menu-bar {
    background-color: #6b21a8; /* Cor do menu */
    padding: 1rem; 
    color: white;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 50;
  }
  
  .container {
    max-width: 1200px; 
    margin: 0 auto; 
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  
  .logo {
    height: 50px; 
    width: auto;
  }
  
  .search-container {
    flex: 1; 
    margin: 0 10rem; 
  }
  
  .search-input {
    width: 100%;
    padding: 0.5rem;
    border: none;
    border-radius: 4px;
    font-size: 0.875rem;
  }
  
  .nav {
    display: flex;
    gap: 2rem; 
  }
  
  .nav-button {
    background: none; 
    border: none; 
    cursor: pointer;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0;
  }
  
  .nav-icon {
    height: 24px;
    width: auto;
    margin-bottom: 0.5rem; 
  }
  
  .nav-text {
    color: white;
    text-align: center;
    font-size: 0.875rem; 
  }
  
  .content {
    padding-top: 80px; /* Espaço suficiente para empurrar o conteúdo abaixo do menu */
    display: flex;
    justify-content: center;
    align-items: center;
    height: calc(100vh - 80px); /* Altura total da tela menos a altura do menu */
  }
  
  .login-container {
    background-color: #f0f0f0; /* Fundo cinza */
    border-radius: 8px; /* Arredonda os cantos */
    padding: 2rem;
    width: 300px; /* Largura da caixa de login */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Sombra sutil para a caixa de login */
    text-align: center; /* Centraliza o texto */
  }
  
  .login-title {
    margin-bottom: 1.5rem; /* Espaçamento abaixo do título */
  }
  
  .input-field {
    width: 100%; /* Largura total do campo de entrada */
    padding: 0.5rem;
    border: 1px solid #ccc; /* Borda cinza */
    border-radius: 4px;
    margin-bottom: 1rem; /* Espaçamento abaixo do campo */
  }
  
  .login-button {
    background-color: #6b21a8; /* Cor do botão */
    color: white;
    border: none;
    border-radius: 4px;
    padding: 0.5rem;
    cursor: pointer;
    width: 100%; 
  }
  
  .login-button:hover {
    background-color: #5a189a;
  }
  
  .login-footer {
    margin-top: 1rem; 
  }
  
  .register-link {
    color: #6b21a8; 
    text-decoration: underline; 
  }
  </style>
  