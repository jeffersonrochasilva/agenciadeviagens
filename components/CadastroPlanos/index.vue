<template>
  <div class="container">
    <div class="span"><span>Contrate seu plano</span></div>
    <div class="container-form">
      <div>
        <input v-model="nomeone" type="name" placeholder="Digite seu nome" />
      </div>
      <div>
        <input
          v-model="sobrenomeone"
          type="name"
          placeholder="Digite seu sobrenome"
        />
      </div>
      <div>
        <input
          v-model="emailone"
          type="e-mail"
          placeholder="Digite seu E-mail"
        />
      </div>
      <div>
        <input
          v-model="senhaone"
          type="password"
          placeholder="Digite sua senha"
        />
      </div>
      <div>
        <input
          v-model="senhaone"
          type="password"
          placeholder="Confirme sua senha"
        />
      </div>
      <div class="button">
        <button @click="modalShow">Cadastrar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nomeone: "",
      sobrenomeone: "",
      emailone: "",
      senhaone: ""
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
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}
.span {
  height: 70px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.span span {
  font-size: 32px;
  font-style: italic;
}

.container-form {
  width: 100%;
  height: 90%;
  display: flex;

  justify-content: center;
  justify-content: space-around;
  flex-direction: column;
}
.container-form input {
  width: 80%;
  height: 60px;
  font-size: 16px;
  text-align: center;
  margin-left: 70px;
  border-style: none;
  border-radius: 8px;
  background: #fff;
}

.button {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.button button {
  width: 130px;
  height: 30px;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
  border-radius: 8px;
  border-style: none;
}
</style>
