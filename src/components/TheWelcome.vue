<script >
import mission from '../components/Mission.vue'
import vision from '../components/Vission.vue'
import { RouterLink, RouterView } from 'vue-router'

export default{
components:{
  mission,
  vision,
},
data(){
  return {
    items: [
      {img: 'https://res.cloudinary.com/difrw7gue/image/upload/v1670435512/P2_txiln9.png', title: 'Mis proyectos', p: 'Individuales', to: '/projects'},
      {img: 'https://res.cloudinary.com/difrw7gue/image/upload/v1670438843/htmlCard_obnwbq.jpg', title: 'Lenguajes de programación', p: 'Conocimiento', to: '/languages'},
      {img: 'https://res.cloudinary.com/difrw7gue/image/upload/v1670520616/Mision-y-Vision.jpg_wmhkd4.jpg', title: 'Misión y Visión', p: 'personal', to: '/mv'},
    ]
  }
},

}
</script>

<template>
  <div class="mainCont">
    <div class="cont-l">
      <h1>Andrés Quesada</h1>
      <h1>Desarrollador en Software</h1>
      <p>Bienvenidos a mi portafolio amantes del software <br>Soy un apasionado del software, desde el 2020 <br> inició mi aventura. Buscando mejorar y automatizar <br> tareas para el mundo, siempre con calidad. <br> Para saber más, </p>
      <RouterLink class="twm" to="/contact"><span><p>Habla conmigo &#10230;</p></span></RouterLink>
    </div>
    <div class="cont-r">
      <img class="img" src="https://res.cloudinary.com/difrw7gue/image/upload/v1670557002/png_20221208_204403_0000_pw1azy.jpg" alt="">
      <span><p class="dl"><a href="../../public/Curriculum - Andres Quesada Arias.pdf" target="_blank">Descarga mi CV &#10230;</a></p></span> 
    </div>
  </div>
  <div class="mainCont2">
    <div class="cont-l2">
      <h1>Mi trabajo</h1>
      <p>Mi principal fuerte es el desarrollo backend, de tal manera que pueda ofrecer la mejor solución al cliente. Todo esto, junto con frameworks populares que van evolucionando para el desarrollo UI. <br><br> Parte de mi compromiso con el cliente es ofrecer las siguientes caracteristicas en mis trabajos:</p>
      <br>
      <p class="orange">Calidad</p>
      <p class="orange">Responsabilidad</p>
      <p class="orange">Compromiso</p>
      <p class="orange">Adaptabilidad</p>
    </div>

    <div class="cont-r2">
      <div v-for="item in items" class="subCont2">
        <img class="img2" :src="item.img">
        <div style="width: 50%">
          <h6 class="text">{{item.title}}</h6>
          <p class="text">{{item.p}}</p>
        </div>
        <div class="arrow">
          <RouterLink :to="{path:item.to}"><span><p>&#10230;</p></span></RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.orange{
  color: rgb(228, 151, 9);
}
a{
  text-decoration: none;
  color: rgb(228, 151, 9);
}
.arrow{
  text-align: right;
  width: 20%;
  padding: 30px;
  color: rgb(228, 151, 9);
}
.img2{
  height: 60px;
  width: 80px;
}
.text{
  padding-left: 30px;
}
.subCont2{
  width: 93%;
  display: flex;
  border-bottom: 0.5px solid rgb(100, 100, 100);
  margin-bottom: 30px;
}
.mainCont2{
  color: #e2cfcf;
  display: flex;
  margin-top: 50px;
  margin-bottom: 50px;
}
.cont-l2{
  width: 40%;
  padding-left: 40px;
  padding-top: 20px;
}

.cont-r2{
  background-color: #222225;
  width: 60%;
  padding: 30px;
  padding-left: 60px;
  height: 500px;
}

.twm{
  text-decoration: none;
  color: rgb(228, 151, 9);
}
.mainCont{
  overflow: hidden;
  padding-bottom: 20px;
  display: flex;
  color: rgb(226, 207, 207);
}
.img{
  height: 320px;
  width: 270px;
  max-height: 400px;
  margin-left: -200px;
  margin-top: 50px;
  filter: grayscale(50%);
}

.cont-l{
  width: 60%;
  padding: 30px;
  padding-left: 40px;
  height: 400px;
  z-index: 4;
}

.dl{
  float: right;
  padding-right: 200px;
  padding-top: 100px;
}
.cont-r{
  position: absolute;
  right: 0;
  top: 0;
  z-index: 3;
  background-color: rgb(33, 33, 36);
  width: 40%;
  height: 300px;
  color: rgb(228, 151, 9);
}
</style>
