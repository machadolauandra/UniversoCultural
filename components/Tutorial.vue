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
          <nuxt-link to="/Conta" class="nav-button"> <!-- Alterado para direcionar para /Conta -->
            <img src="/user.png" alt="Conta" class="nav-icon" />
            <span class="nav-text">Conta</span>
          </nuxt-link>
        </nav>
      </div>
    </div>

    <div class="content">
      <div class="squares-container">
        <div class="square">
          <img src="assim.jpg" alt="Imagem 1" class="square-image" />
          <p class="square-text">É ASSIM QUE ACABA</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="comeca.jpg" alt="Imagem 2" class="square-image" />
          <p class="square-text">É ASSIM QUE COMEÇA</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="/invisivel.jpg" alt="Imagem 3" class="square-image" />
          <p class="square-text">As vantagens de ser invisível</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="/lado.jpg" alt="Imagem 4" class="square-image" />
          <p class="square-text">O LADO FEIO DO AMOR</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="/biblioteca.jpg" alt="Biblioteca da meia noite" class="square-image" />
          <p class="square-text"> A biblioteca da meia noite</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="/imperfeicoes.jpg" alt="Imagem 6" class="square-image" />
          <p class="square-text">Todas as suas imperfeições</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="/maridos.jpg" alt="Imagem 7" class="square-image" />
          <p class="square-text">Os sete maridos de Evelyn Hugo</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
        <div class="square">
          <img src="/partes.jpg" alt="Imagem 8" class="square-image" />
          <p class="square-text">As mil partes do meu coração</p>
          <div class="square-buttons">
            <button class="square-button">Comprar</button>
            <div class="carrinho-favorite">
              <button class="square-button">Carrinho</button>
              <img src="/coracao.png" alt="Favorito" class="favorite-icon" />
            </div>
          </div>
        </div>
      </div>
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

.nav-button:hover .nav-text {
  text-decoration: underline; 
}

.content {
  padding-top: 80px;
}

.squares-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
  padding: 1rem; 
}

.square {
  background-color: #f0f0f0; 
  border-radius: 8px; 
  padding: 1rem;
  width: calc(25% - 1rem); 
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.square-image {
  width: 100%;
  height: auto;
  max-width: 150px; 
}
.square-text {
  margin: 1rem 0;
  text-align: center; 
}

.square-buttons {
  display: flex;
  gap: 0.5rem; 
}

.carrinho-favorite {
  display: flex;
  align-items: center; 
}

.favorite-icon {
  height: 24px; 
  width: auto;
  margin-left: 0.5rem; 
}
</style>
