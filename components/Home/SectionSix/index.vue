<template>
  <section class="section-container">
    <div class="container">
      <div class="title">
        <span>Depoimentos</span>
      </div>
      <div class="container-depoimentos-one">
        <div class="depoimento-one">
          <img src="@/assets/mulher1.jpeg" alt="" />
          <div>
            <p>Viagem feita para Salvador</p>
            <button @click="infoModal">Saiba mais</button>
          </div>
        </div>
      </div>
      <div class="container-depoimentos-two">
        <div class="depoimento-two">
          <div>
            <p>Viagem feita para Paris</p>
            <button @click="infoModal">Saiba mais</button>
          </div>
          <img src="@/assets/mulher2.jpeg" alt="" />
        </div>
      </div>
      <div class="container-depoimentos-one">
        <div class="depoimento-one">
          <img src="@/assets/mulher3.jpeg" alt="" />
          <div>
            <p>Viagem feita para New york</p>
            <button @click="infoModal">Saiba mais</button>
          </div>
        </div>
      </div>
      <div class="container-depoimentos-two">
        <div class="depoimento-two">
          <div>
            <p>Viagem feita para Argentina</p>
            <button @click="infoModal">Saiba mais</button>
          </div>
          <img src="@/assets/mulher4.jpeg" alt="" />
        </div>
      </div>
    </div>
    <div v-if="informationModal" class="overlay" />
    <div v-if="informationModal" class="modal-wrapper">
      <div class="information-container">
        <Information :information-Modal="infoModal" />
      </div>
    </div>
  </section>
</template>

<script>
import Information from "@/components/Information";

export default {
  data: () => ({
    informationModal: false
  }),
  methods: {
    infoModal() {
      this.informationModal = !this.informationModal;
    }
  },
  components: {
    Information
  }
};
</script>

<style scoped>
@keyframes animation {
  0% {
    left: 0;
  }
  50% {
    left: 817px;
  }
  100% {
    left: 0px;
  }
}
@keyframes animation2 {
  0% {
    right: 0;
  }
  50% {
    right: 817px;
  }
  100% {
    right: 0px;
  }
}
.section-container {
  width: 100%;
  height: 1000px;
  background: #f0f2f8;
  display: flex;
  justify-content: center;
}

.title {
  max-width: 1170px;
  height: 100px;
}

.title span {
  font-size: 50px;
  color: green;
}

.container {
  width: 1170px;
}

.container-depoimentos-one {
  max-width: 1170px;
}

.container-depoimentos-two {
  max-width: 1170px;
  display: flex;
  justify-content: flex-end;
}

.depoimento-two {
  width: 330px;
  height: 230px;
  display: flex;
  animation-name: animation2;
  animation-duration: 5s;
  position: relative;
  animation-iteration-count: infinite;
  animation-timing-function: ease;
}

.depoimento-one {
  width: 330px;
  height: 230px;
  display: flex;
  animation-name: animation;
  animation-duration: 5s;
  position: relative;
  animation-iteration-count: infinite;
  animation-timing-function: ease;
}

.depoimento-two div {
  height: 230px;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.depoimento-one div {
  height: 230px;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.depoimento-two div button {
  width: 110px;
  height: 30px;
  font-family: sans-serif;
  border-radius: 8px;
  border-style: none;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
}

.depoimento-one div button {
  width: 110px;
  height: 30px;
  font-family: sans-serif;
  border-radius: 8px;
  border-style: none;
  background: linear-gradient(180deg, #00f260 0%, #0575e6 100%);
  cursor: pointer;
}

.depoimento-two div p {
  font-family: sans-serif;
}
.depoimento-one div p {
  font-family: sans-serif;
}
.depoimento-two img {
  width: 200px;
  height: 200px;
  border-radius: 8px;
}
.depoimento-one img {
  width: 200px;
  height: 200px;
  border-radius: 8px;
}

/* style da modal*/

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
