<template>
  <BasicLayouts>
  <div class="banner"></div>
  <div class="services">
    <h1>Ofrecemos Nuestros Servicios a tu Alcance</h1>
  </div>
  <section class="services-section">
    <article>
      <router-link class="item" to="/">
        <img src="../assets/soluciones-informaticas.jpg" alt="Soluciones Informáticas" />
      </router-link>
      <h2>Soluciones Informáticas</h2>
      <p class="parrafo">
        Transmision de datos y video a largas distancias implementando redes
        inalámbricas con tecnologías microondas
      </p>
    </article>

    <article>
      <router-link class="item" to="/">
        <img src="../assets/soluciones-leasing.jpg" alt="Soluciones Leasing" />
      </router-link>
      <h2>Soluciones Leasing</h2>
      <p class="parrafo">
        Implemente las soluciones tecnologias mas avanzadas en seguridad
        electrónica para vigilar su negocio y hogar.
      </p>
    </article>

    <article class="domotica">
      <router-link class="item" to="/">
        <img src="../assets/soluciones-soporte.jpeg" alt="Soluciones en Soporte" />
      </router-link>
      <h2>Soluciones en Soporte</h2>
      <p class="parrafo">
        Diseñe una casa inteligente con la mas avanzada tecnología domotica en
        control e iluminación.
      </p>
    </article>
  </section>
</BasicLayouts>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useRouter } from 'vue-router';
import BasicLayouts from '../layouts/BasicLayouts.vue';
import {} from '../api/category';

export default {
  name: 'Inicio',
  components: {
    BasicLayouts,
  },
};
</script>

<style lang="scss" scoped>
.banner {
  background-position: center;
  background-size: cover;
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: flex-end;
  flex-direction: column;
  text-align: center;
  height: 400px;
  background-image: url('../assets/Portada.jpg');
}

.services {
  background-color: #16202b;
  height: 100px;
  color: white;
  /*Para centrar un contenido*/
  display: flex;
  justify-content: center;
  align-items: center;
}

.header-container {
  background-color: #f7f7f7;
}

.services-section {
  display: flex;
  align-items: center;
}

.services-section article {
  padding: 20px;
  text-align: center;
}

.services-section img {
  border-radius: 60%;
  margin-right: auto;
  margin-left: auto;
  width: 60%;
  height: 60%;
  margin-bottom: 30px;
}

.domotica {
  margin-bottom: 10px;
}
.services-section p {
  font-size: 20px;
  text-align: justify;
}
</style>
