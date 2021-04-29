<template>
  <section id="section-three">
    <div class="three-container">
      <span>Destinos</span>
      <div class="bens">
        <div class="items">
          <img src="@/assets/unnamed.jpg" alt="" />
          <strong>Paisagen 01</strong>
          <p>
            Lorem Ipsum é simplesmente uma simulação de texto da indústria
            tipográfica e de impressos, e vem sendo utilizado desde
          </p>
          <button @click="handleModal">Conheça</button>
        </div>
        <div class="items">
          <img src="@/assets/dsc_2320.jpg" alt="" />
          <strong>Paisagen 01</strong>
          <p>
            Lorem Ipsum é simplesmente uma simulação de texto da indústria
            tipográfica e de impressos, e vem sendo utilizado desde
          </p>
          <button @click="handleModal">Conheça</button>
        </div>
        <div class="items">
          <img src="@/assets/images.jpg" alt="" />
          <strong>Paisagen 01</strong>
          <p>
            Lorem Ipsum é simplesmente uma simulação de texto da indústria
            tipográfica e de impressos, e vem sendo utilizado desde
          </p>
          <button @click="handleModal">Conheça</button>
        </div>
      </div>
    </div>
    <div>
      <div v-if="conhecaNosModal" class="overlay" />
      <div v-if="conhecaNosModal" class="modal-wrapper">
        <div class="information-container">
          <ConhecaNos :show-modal="handleModal" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ConhecaNos from "@/components/ConhecaNos";
export default {
  data: () => ({
    conhecaNosModal: false
  }),
  methods: {
    handleModal() {
      this.conhecaNosModal = !this.conhecaNosModal;
    }
  },
  components: {
    ConhecaNos
  }
};
</script>

<style scoped>
#section-three {
  height: 573px;
  width: 100%;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
}
#section-three .three-container {
  width: 100%;
  height: 100%;
  max-width: 1170px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}
#section-three .three-container span {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 80px;
}
#section-three .three-container .bens {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
#section-three .three-container .bens .items {
  width: 221px;
  height: 290px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}
#section-three .three-container .bens .items img {
  width: 126px;
  height: 138px;
  border-radius: 14px;
}
#section-three .three-container .bens .items strong {
  font-size: 22px;
}
#section-three .three-container .bens .items p {
  font-size: 16px;
  text-align: center;
}

#section-three .three-container .bens .items button {
  width: 120px;
  height: 30px;
  border: none;
  border-radius: 8px;
  text-align: center;
  cursor: pointer;
  background: #000;
  color: #fff;
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
