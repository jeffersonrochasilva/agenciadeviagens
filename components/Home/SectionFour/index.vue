<template>
  <section id="section-four">
    <div class="container">
      <div class="container-span">
        <span>Nossos Planos</span>
      </div>
      <div class="container-plans">
        <div class="plans-one">
          <span>Mensal</span>
          <div class="div-monthly-value">
            <p>R$</p>
            <p class="monthly-value">19,90</p>
            <p>/mês</p>
          </div>
          <ul>
            <li>Consulta por videochamada</li>
            <li>Renovação de receita médica</li>
            <li>Descontos em exames</li>
          </ul>
          <button @click="handleModal">Cadastrar agora</button>
        </div>
        <div class="plans-one">
          <span>Anual</span>
          <div class="div-monthly-value">
            <p>R$</p>
            <p class="monthly-value">14,90</p>
            <p>/mês</p>
          </div>
          <ul>
            <li>Consulta por videochamada</li>
            <li>Renovação de receita médica</li>
            <li>Descontos em exames</li>
          </ul>
          <button @click="handleModal">Cadastrar agora</button>
        </div>
        <div class="plans-one">
          <span>Semestral</span>
          <div class="div-monthly-value">
            <p>R$</p>
            <p class="monthly-value">16,90</p>
            <p>/mês</p>
          </div>
          <ul>
            <li>Consulta por videochamada</li>
            <li>Renovação de receita médica</li>
            <li>Descontos em exames</li>
          </ul>
          <button @click="handleModal">Cadastrar agora</button>
        </div>
      </div>
    </div>
    <div>
      <div v-if="modalTeste" class="overlay" />
      <div v-if="modalTeste" class="modal-wrapper">
        <div class="information-container">
          <CadastroPlanos :modal-show="handleModal" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import CadastroPlanos from "@/components/CadastroPlanos";
export default {
  data: () => ({
    modalTeste: false
  }),
  methods: {
    handleModal() {
      this.modalTeste = !this.modalTeste;
    }
  },
  components: {
    CadastroPlanos
  }
};
</script>

<style scoped>
#section-four {
  max-width: 100%;
  height: 722px;
  padding: 50px;
  background: #f0f2f8;
  display: flex;
  justify-content: center;
}

.container {
  max-width: 1170px;
  height: 100%;
  background: #f0f2f8;
}
#section-four .container-span {
  margin-bottom: 1px solid #f0f2f8;
}
#section-four .container-span span {
  font-size: 42px;
  font-family: poppins;
}
#section-four .container-plans {
  margin-top: 10px;
  display: flex;
  justify-content: space-around;
}

#section-four .container-plans .div-monthly-value {
  display: flex;
  align-items: flex-end;
}

#section-four .container-plans .div-monthly-value .monthly-value {
  font-size: 64px;
  color: #fff;
}
#section-four .container-plans .div-monthly-value p {
  color: #fff;
}
#section-four .container-plans .plans-one {
  width: 360px;
  height: 519px;
  margin: 10px;
  padding: 22px 22px 22px 35px;
  border-radius: 10px;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  justify-content: space-around;
}
#section-four .container-plans .plans-one span {
  font-size: 25px;
  font-family: poppins;
}
#section-four .container-plans .plans-one button {
  width: 290px;
  height: 40px;
  border-radius: 8px;
  background: #000;
  color: #fff;
  cursor: pointer;
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

/* stule da modal*/

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
