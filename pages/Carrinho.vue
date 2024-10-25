<template>
    <div>
      <div class="menu-bar">
        <div class="container">
            <nuxt-link to="/" class="nav-button">
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
                <nuxt-link to="/Favoritos" class="nav-button">
              <img src="/favorite.png" alt="Favoritos" class="nav-icon" />
              <span class="nav-text">Favoritos</span>
                </nuxt-link>
            </button>
            <nuxt-link to="/Conta" class="nav-button">
              <img src="/user.png" alt="Conta" class="nav-icon" />
              <span class="nav-text">Conta</span>
            </nuxt-link>
          </nav>
        </div>
      </div>
  
      <div class="content">
        <div class="cart-container">
          <h2 class="cart-title">Carrinho de Compras</h2>
          <div v-if="cartItems.length">
            <div class="cart-item" v-for="(item, index) in cartItems" :key="index">
              <img :src="item.image" :alt="item.name" class="cart-item-image" />
              <div class="cart-item-details">
                <p class="cart-item-name">{{ item.name }}</p>
                <p class="cart-item-price">R$ {{ item.price }}</p>
                <button @click="removeFromCart(index)" class="remove-button">Remover</button>
              </div>
            </div>
            <div class="cart-total">
              <p>Total: R$ {{ totalPrice }}</p>
            </div>
            <button class="checkout-button">Finalizar Compra</button>
          </div>
          <div v-else>
            <p>Seu carrinho está vazio.</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        cartItems: [
          { name: 'É ASSIM QUE ACABA', price: 29.99, image: 'assim.jpg' },
          { name: 'O LADO FEIO DO AMOR', price: 39.99, image: 'lado.jpg' }
        ]
      }
    },
    computed: {
      totalPrice() {
        return this.cartItems.reduce((acc, item) => acc + item.price, 0).toFixed(2);
      }
    },
    methods: {
      removeFromCart(index) {
        this.cartItems.splice(index, 1);
      }
    }
  }
  </script>
  
  <style scoped>
  .menu-bar {
    background-color: #5a189a;
    padding: 1rem;
    color: white;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 50;
    box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.1);
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
    border: 1px solid #ddd;
    border-radius: 20px;
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
    color: #e0e0e0;
    text-align: center;
    font-size: 0.9rem;
    font-weight: 500;
  }
  
  .content {
    padding-top: 80px;
  }
  
  .cart-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 1rem;
  }
  
  .cart-title {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 1rem;
    text-align: center;
  }
  
  .cart-item {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
    border: 1px solid #ddd;
    padding: 1rem;
    border-radius: 8px;
  }
  
  .cart-item-image {
    height: 60px;
    width: auto;
    margin-right: 1rem;
  }
  
  .cart-item-details {
    flex: 1;
  }
  
  .cart-item-name {
    font-size: 1rem;
    font-weight: bold;
  }
  
  .cart-item-price {
    color: #6b21a8;
  }
  
  .remove-button {
    background-color: #f87171;
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 8px;
    cursor: pointer;
    font-size: 0.875rem;
    margin-top: 0.5rem;
  }
  
  .cart-total {
    font-size: 1.25rem;
    font-weight: bold;
    text-align: right;
    margin-top: 1rem;
  }
  
  .checkout-button {
    background-color: #6b21a8;
    color: white;
    width: 100%;
    border: none;
    padding: 1rem;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    margin-top: 1rem;
  }
  
  .checkout-button:hover {
    background-color: #5a189a;
  }
  </style>
  