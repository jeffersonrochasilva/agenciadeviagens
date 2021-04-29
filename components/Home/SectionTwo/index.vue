<template>
  <section id="section-two">
    <div class="left">
      <div class="img">
        <img src="@/assets/viegen3.jpeg" alt="" />
      </div>
    </div>
    <div class="right">
      <span>Qual lugar você quer conhecer hoje ?</span>
      <p>
        A NPM tem os melhores planos de viagens! Veja qual se adequa mais a
        você.
      </p>
      <p>
        Vamos começar ?
      </p>
    </div>
  </section>
</template>

<style scoped>
#section-two {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 100px 0;
}

#section-two .img img {
  width: 617px;
  height: 362px;
  border-radius: 14px;
}
#section-two .right {
  height: 210px;
  width: 40%;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-direction: column;
}
#section-two .right span {
  font-size: 32px;
}
#section-two .right p {
  font-size: 18px;
}
</style>
