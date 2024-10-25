<template>
  <div>
    <div class="menu-bar">
      <div class="container">
        <nuxt-link to="/">
          <img src="/logo.png" alt="Logo" class="logo" />
        </nuxt-link>
        <div class="search-container">
          <input type="text" placeholder="O que você está procurando?" class="search-input" />
        </div>
        <nav class="nav">
          <button class="nav-button">
            <nuxt-link to="/Carrinho" class="nav-button">
            <img src="carrinho.png" alt="Carrinho" class="nav-icon" />
            <span class="nav-text">Carrinho</span>
            </nuxt-link>
          </button>
          <button class="nav-button">
            <img src="/favorite.png" alt="Favoritos" class="nav-icon" />
            <span class="nav-text">Favoritos</span>
          </button>
          <nuxt-link to="/Conta" class="nav-button"> 
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
            Não tem uma conta? <router-link to="/Cadastro" class="register-link">Cadastre-se</router-link>
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
html, body {
  height: 100%;
  margin: 0;
}

.menu-bar {
  background-color: #6b21a8;
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
  padding-top: 80px; 
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh; 
  background-color: #f0f0f0; 
}

.login-container {
  background-color: #ffffff; 
  border-radius: 10px; 
  padding: 2rem;
  width: 300px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1); 
  text-align: center;
  transition: box-shadow 0.3s ease; 
}

.login-container:hover {
  box-shadow: 0 6px 30px rgba(0, 0, 0, 0.2);
}

.login-title {
  color: #6b21a8;
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  font-weight: bold; 
}

.input-field {
  width: 100%;
  padding: 0.75rem; 
  border: 1px solid #ccc;
  border-radius: 5px; 
  margin-bottom: 1rem;
  font-size: 1rem; 
  transition: border 0.3s ease; 
}

.input-field:focus {
  border-color: #6b21a8; 
  outline: none; 
  box-shadow: 0 0 5px rgba(107, 33, 168, 0.5); 
}

.login-button {
  background-color: #6b21a8;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 0.75rem;
  cursor: pointer;
  width: 100%; 
  font-size: 1rem;
  transition: background-color 0.3s ease; 
}

.login-button:hover {
  background-color: #5a189a; 
}

.login-footer {
  margin-top: 1rem; 
  font-size: 0.9rem; 
  color: #666;
}

.register-link {
  color: #6b21a8; 
  text-decoration: underline; 
  font-weight: bold; 
}
</style>
