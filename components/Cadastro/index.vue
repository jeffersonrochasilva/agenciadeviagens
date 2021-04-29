<template>
  <div class="container">
    <div class="container-cadastro">
      <div class="div-header">
        <div class="title"><h1>Cadastro</h1></div>
        <div class="img-close">
          <button @click="modalShow" class="close-button">
            <img src="@/assets/fechamento.jpeg" alt="" />
          </button>
        </div>
      </div>

      <form class="container-form">
        <input type="text" v-model="nome" placeholder="Digite seu nome" />
        <input
          type="text"
          v-model="sobrenome"
          placeholder="Digite seu sobrenome"
        />
        <input type="email" v-model="email" placeholder="Digite seu E-mail" />
        <input type="password" v-model="senha" placeholder="Digite sua senha" />
        <input
          type="password"
          v-model="senha"
          placeholder="Confirme sua senha"
        />
      </form>
      <div class="div-button">
        <button @click="modalShow" type="submit" class="button-form">
          Cadastrar
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nome: "",
      sobrenome: "",
      email: "",
      senha: ""
    };
  },
  props: {
    modalShow: Boolean
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 100%;
  background: #f0f2f8;
}

.div-header {
  width: 100%;

  display: flex;
  justify-content: space-around;
  align-items: center;
}
.close-button {
  border: none;
  cursor: pointer;
}
.close-button img {
  width: 20px;
  height: 20px;
}
.container-cadastro {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;

  align-items: center;
}
.container-form {
  width: 90%;

  display: flex;
  justify-content: space-around;
  flex-direction: column;
  justify-content: space-between;
}

.container-form input {
  width: 100%;
  height: 60px;
  text-align: center;
  border: none;
  border-radius: 8px;
  margin: 10px;
}

.div-button {
  width: 100%;

  display: flex;
  justify-content: center;
}

.div-button button {
  width: 90px;
  height: 35px;
  border: none;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
  border-radius: 8px;
}
</style>
