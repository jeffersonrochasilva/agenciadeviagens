<template>
  <section id="section-one">
    <div class="left">
      <span>
        Viva a experiencia de viajar conosco !
      </span>
      <p>Texto secundeario do site</p>
      <a href="">Veja mais </a>
    </div>
    <div class="right">
      <div class="img">
        <img src="@/assets/viajem.jpeg" alt="" />
      </div>
    </div>
  </section>
</template>

<style scoped>
#section-one {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 100px 0;
}
#section-one .left {
  height: 200px;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;
  flex-direction: column;
}
#section-one .left span {
  font-size: 40px;
}
#section-one .left p {
  font-size: 28px;
}
#section-one .left a {
  font-size: 16px;
  text-decoration: none;
  color: #ff0000;
}

#section-one .right .img img {
  width: 672px;
  height: 505px;
  border-radius: 14px;
}
</style>
