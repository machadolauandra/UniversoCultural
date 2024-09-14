<template>
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
        <button class="nav-button">
          <img src="/user.png" alt="Conta" class="nav-icon" />
          <span class="nav-text">Conta</span>
        </button>
      </nav>
    </div>
  </div>
</template>

<style scoped>
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
  flex: 1; /* Faz com que o container da barra de pesquisa ocupe o espaço disponível entre o logo e a navegação */
  margin: 0 10rem; /* Adiciona espaço entre a barra de pesquisa e os botões de navegação */
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
  font-size: 0.875rem; /* Ajuste o tamanho da fonte conforme necessário */
}

.nav-button:hover .nav-text {
  text-decoration: underline; /* Adiciona sublinhado ao texto no hover */
}
</style>
