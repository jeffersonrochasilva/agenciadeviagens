<template>
  <nav>
    <ul>
      <li><a href="">O que é</a></li>
      <li><a href="">Benefícios</a></li>
      <li><a href="">Como funciona</a></li>
      <li><a href="">Planos</a></li>
      <li><a href="">Depoimentos</a></li>
      <li><a href="">Na mídia</a></li>
      <li><button @click="handleModal">Cadastrar</button></li>
    </ul>
    <div>
      <div v-if="showModal" class="overlay" />
      <div v-if="showModal" class="modal-wrapper">
        <div class="information-container">
          <Cadastro :modal-show="handleModal" />
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import Cadastro from "@/components/Cadastro";
export default {
  data: () => ({
    showModal: false
  }),
  methods: {
    handleModal() {
      this.showModal = !this.showModal;
    }
  },
  components: {
    Cadastro
  }
};
</script>

<style scoped>
nav {
  width: 100%;
  display: flex;
  justify-content: flex-end;
}
nav ul {
  width: 70%;
  display: flex;
  justify-content: space-between;
}

nav ul li {
  list-style: none;
}

nav ul li button {
  width: 115px;
  height: 25px;
  border-right: 10px;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);

  cursor: pointer;
  border: none;
}

nav ul li a {
  text-decoration: none;
  color: #000;
}
.overlay {
  width: 9999px;
  height: 9999px;
  background: rgba(255, 255, 255, 0.75);
  backdrop-filter: blur(20px);
  top: 0;
  left: 0;
  transform: translate(-50%, -50%);
  position: fixed;
  z-index: 99999;
}

.modal-wrapper {
  position: fixed;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 10vh;
  left: 0;
  top: 0;
  z-index: 999999;
  color: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
}

.information-container {
  width: 90%;
  height: 90vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 800px;
  margin: 0 auto;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
  padding: 10px;
  border-radius: 10px;
  margin-top: 50px;
}
</style>
