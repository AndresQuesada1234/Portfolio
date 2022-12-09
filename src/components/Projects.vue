<script>
  import { ref } from "vue";
  import { MDBCarousel } from "mdb-vue-ui-kit";

  export default {
    components: {
      MDBCarousel
    },
    setup() {
      const items1 = [
        {
          src: "https://res.cloudinary.com/difrw7gue/image/upload/v1670435242/P1_q1isun.png",
          alt: "...",
          label: "Gym App",
          caption: "Aplicación para el manejo de rutinas"
        },
        {
          src: "https://res.cloudinary.com/difrw7gue/image/upload/v1670435512/P2_txiln9.png",
          alt: "...",
          label: "Mi cocina",
          caption: "Aplicación para guardar recetas de cocina"
        },
        {
          src: "https://res.cloudinary.com/difrw7gue/image/upload/v1670435722/p3_urs6hy.png",
          alt: "...",
          label: "Consultoría Informatica",
          caption:
            "Aplicación informativa de consultoría informatica."
        }
      ];
      const carousel1 = ref(0);
      return {
        items1,
        carousel1
      };
    }
  };
</script>
<template>
    <MDBCarousel 
      v-model="carousel1"
      :items="items1"
      fade
    />
</template>

<style scoped>
h1{
    text-align: center;
    padding: 10px;
    margin: 0;
}
</style>