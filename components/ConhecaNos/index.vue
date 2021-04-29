<template>
  <div class="container">
    <div class="container-top">
      <div class="containe-one">
        <img src="@/assets/passeiodebugue.jpeg" alt="passeiodebugue" />
        <p>Os melhores passeios, com os melhores preços pra você.</p>
      </div>
      <div class="container-two">
        <p>O melhor cerviço de hospedagem do mercado.</p>
        <img src="@/assets/camareira.jpeg" alt="camareira" />
      </div>
      <div class="container-three">
        <img src="@/assets/festa.jpeg" alt="festa" />
        <p>Os melhores ambientes para festas, com muita seguraça e diversão.</p>
      </div>
    </div>
    <div class="lista-beneficios">
      <div>
        <ul>
          <li>Mais de 40 anos de mercado</li>
          <li>Mais de 20 mil clientes satisfeitos</li>
          <li>98% de satisfação dos clientes</li>
          <li>Empresa com sede em todo o Brasil</li>
          <li>Cancelamentos sem taxa</li>
        </ul>
      </div>
      <div>
        <button @click="showModal">Voltar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    showModal: Boolean
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 100%;
}

.container-top p {
  font-size: 17px;
  font-family: Arial, Helvetica, sans-serif;
}

.containe-one {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.containe-one img {
  width: 220px;
  height: 140px;
  border-radius: 8px;
}

.container-two {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.container-two img {
  width: 220px;
  height: 140px;
  border-radius: 8px;
}
.container-three {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.container-three img {
  width: 220px;
  height: 140px;
  border-radius: 8px;
}

.lista-beneficios {
  padding-top: 10px;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}

.lista-beneficios button {
  width: 110px;
  height: 30px;
  margin-right: 8px;
  border-radius: 8px;
  border-style: none;
  background: #000;
  color: #fff;
}

.lista-beneficios li {
  font-family: poppins;
  font-size: 16px;
  font-style: none;
}
</style>
