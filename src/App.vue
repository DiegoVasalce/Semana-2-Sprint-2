<template>
  <div class="container">
    <!--Seccion superior-->

    <!--Seccion de noticias-->
    <div id="news">
      <componente-noticias></componente-noticias>
    </div>

    <!--Seccion de equipos-->
    <div id="team" class="card-deck">
      <team-card
        v-for="(member, index) of members"
        :key="index"
        :member="member"
      ></team-card>
    </div>

    <!--Seccion Footer-->
    <div id="footer">
      <footer-section></footer-section>
    </div>
 </div>
</template>

<script>
import ComponenteNoticias from "./components/ComponenteNoticias.vue";
import FooterSection from "./components/FooterSection.vue";
import TeamCard from "./components/TeamCard.vue";
export default {
  name: "App",
  components: {
    ComponenteNoticias,
    TeamCard,
    FooterSection,
  },
  data() {
    return {
      members: [
        {
          
        },
        {
          codigo: "1",
          nombre: "Juan Diego Vasquez Salcedo",
          descripcion:
            "Ingeniero Electronico, Que le encanta aprender cada dia mas, Fan del Futbol y los Videojuegos",
          rol: "Desarrollador FullStack",
          image: "./images/foto.jpg",
        },
        
        {
          
        },
      ],
    };
  },
};
</script>

<style></style>

