<template>
    <div class="home-container">
      <h1>Bem-vindo à Página Inicial!</h1>
      <p>Este é um exemplo simples de uma página inicial com estilo.</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Home'
  };
  </script>
  
  <style scoped>
  .home-container {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centraliza horizontalmente */
    padding: 20px;
    background-color: #f0f0f0; /* Um fundo cinza claro */
    border-radius: 8px; /* Bordas arredondadas */
  }
  
  h1 {
    color: #333; /* Cor do título */
    margin-bottom: 10px;
  }
  </style>