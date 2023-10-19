<template>
    <div class="login-card">
      <div class="card-header">
        <h2>Cadastro de Nota de Crédito</h2>
      </div>
      <form @submit.prevent="cadastrarNotaDeCredito" class="card-content">
        <div class="input-container">
          <label for="codigoNotaCredito">Código da Nota de Crédito:</label>
          <input type="text" id="codigoNotaCredito" v-model="codigoNotaCredito" required class="small-input" maxlength="50">
        </div>
  
        <div class="input-container">
          <label for="pi">PI:</label>
          <input type="text" id="pi" v-model="pi" required class="small-input" maxlength="50">
        </div>
  
        <div class="input-container">
          <label for="nd">ND (código):</label>
          <input type="text" id="nd" v-model="nd" required class="small-input">
        </div>
  
        <div class="input-container">
          <label for="valorSaldo">Valor do Saldo:</label>
          <input type="number" id="valorSaldo" v-model="valorSaldo" required class="small-input">
        </div>
  
        <div class="input-container">
          <label for="dataVencimento">Data de Vencimento:</label>
          <input type="date" id="dataVencimento" v-model="dataVencimento" required class="small-input">
        </div>
  
        <button type="submit" class="card-button">Cadastrar</button>
      </form>
    </div>
 


  </template>
  
  <script>
  export default {
    data() {
      return {
        codigoNotaCredito: "",
        numeroNotaCredito: "",
        pi: "",
        nd: "",
        valorSaldo: null,
        dataVencimento: "",
      };
    },
    methods: {
      cadastrarNotaDeCredito() {
        // Implemente a lógica para cadastrar a nota de crédito aqui
      },
    },
  };
  </script>

<style scoped>
.login-card {
  border: 1px solid #ccc;
  border-radius: 8px;
  margin: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  max-width: 300px; /* Limitando a largura do card */
  margin: 0 auto; /* Centralizando o card horizontalmente */
}

.card-header {
  background-color: #4285f4;
  color: white;
  text-align: center;
  padding: 16px;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}

.card-content {
  padding: 16px;
}

.input-container {
  margin-bottom: 12px;
}

label {
  font-weight: bold;
}

.small-input {
  width: 90%;
  padding: 6px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.card-button {
  background-color: #4285f4;
  color: white;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card-button:hover {
  background-color: #3575d3;
}
</style>