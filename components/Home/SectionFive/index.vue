<template>
  <section id="section-five">
    <div class="container">
      <div class="header">
        <span>Apoiadores</span>
      </div>
      <div class="supporters-container">
        <div class="supporters">
          <div class="img">
            <img src="@/assets/azul.jpag.jpg" alt="azul-companhia aeria" />
          </div>
          <div class="decription">
            <p>Azul</p>
            <p>Companhia aeria</p>
          </div>
        </div>
        <div class="supporters">
          <div class="img">
            <img src="@/assets/restaurant.jpeg" alt="restaurante" />
          </div>
          <div class="decription">
            <p>Kicarne restaurants</p>
            <p>A melhor comida do estado!</p>
          </div>
        </div>
        <div class="supporters">
          <div class="img">
            <img src="@/assets/mergulho.jpeg" alt="Companhia de mergulho" />
          </div>
          <div class="decription">
            <p>Mergulos</p>
            <p>Companhia de mergulho</p>
          </div>
        </div>
        <div class="supporters">
          <div class="img">
            <img src="@/assets/pousada.jpeg" alt="pousada" />
          </div>
          <div class="decription">
            <p>Pousadas Arraial</p>
            <p>Fazendo o melhor, pensando no seu bem</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
#section-five {
  width: 100%;
  height: 700px;
  background: #fff;
  display: flex;
  justify-content: center;
}
#section-five .container {
  max-width: 1170px;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
#section-five .container .header {
  max-width: 1170px;
  height: 100px;
  display: flex;
  padding-top: 40px;
}
#section-five .container .supporters-container {
  width: 100%;
  height: 600px;
  display: flex;
  justify-content: center;
}

#section-five .container .header span {
  font-size: 42px;
}

#section-five .container .supporters {
  width: 270px;
  height: 420px;
  margin: 50px 10px;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  border-radius: 8px;
  background: #f0f2f8;
}
#section-five .container .supporters .div-supporters {
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

#section-five .container .supporters .div-supporters .img {
  width: 100%;
  height: 200px;
  display: flex;
  justify-content: center;
}

#section-five .container .supporters img {
  width: 180px;
  height: 180px;
  border-radius: 50%;
}

#section-five .container .supporters .decription {
  width: 100%;
  height: 200%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

#section-five .container .supporterss .decription p {
  font-size: 32px;
  font-family: sans-serif;
}
</style>
