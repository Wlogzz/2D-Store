<template>
  <!-- Footer -->
  <footer class="section-footer">
    <div class="pie">
      <div class="pie__logo">
        <router-link class="pie__img" to="/">
          <img class="pie__img" src="../assets/Logo_Menu.svg" alt="logo" />
        </router-link>
        <p>2D Store</p>
      </div>
      <nav class="pie__nav">
        <ul class="pie__enlaces">
          <li class="pie__li">
            <router-link class="enlaces" to="/nosotros">
              Nosotros
            </router-link>
          </li>
          <li class="pie__li">
            <router-link class="enlaces" to="/login">
              Únete al equipo
            </router-link>
          </li>
        </ul>
      </nav>
      <nav class="pie__nav">
        <ul class="pie__enlaces">
          <li class="pie__li">
            <router-link class="enlaces" to="/productos">Productos</router-link>
          </li>
          <li class="pie__li">
            <a class="enlaces" href="">Términos y condiciones</a>
          </li>
        </ul>
      </nav>

      <div class="pie__social">
        <div class="pie__contacto">
          <h3 class="contacto">Contáctanos</h3>
        </div>
        <div class="pie__redes">
          <a class="enlace-redes" href="#">
            <i class="facebook square icon"> </i>
          </a>
          <a class="enlace-redes" href="#">
            <i class="instagram icon"></i>
          </a>
          <i class="youtube icon"></i>
          <i class="twitter icon"></i>
        </div>
      </div>
    </div>
    <div class="final">
      <p class="final__texto">
        &copy; 2021 2D Store - Diseño & Desarrollo -> Grupo 63 MinTic UTP -
        SubGrupo 08
      </p>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style>
/* Footer */
.section-footer {
  background: #16202b;
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin-top: 60px;
}

.pie {
  padding: 30px 0;
  display: flex;
  justify-content: center;
}
.pie__logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  flex: 1 1 auto;
  justify-content: center;
  border-right: 1px solid #707070;
  color: #707070;
  font-size: 12px;
}

.pie__img {
  width: 100px;
  height: 100px;
}
.pie__nav {
  display: flex;
  flex: 1 1 auto;
  justify-content: center;
  align-items: center;
}
.pie__enlaces {
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
}
.pie__li {
  list-style-type: none;
}
.enlaces {
  color: #b3b3b3;
  text-decoration: none;
  font-size: 11px;
  line-height: 25px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.enlaces:hover {
  text-decoration: none;
  transition: 0.5s;
  color: #ffa500;
}

.pie__social {
  display: flex;
  flex: 1 1 auto;
  justify-content: center;
  align-items: center;
  border-left: 1px solid #707070;
  flex-direction: column;
  color: #b3b3b3;
}
.pie__contacto {
  display: flex;
  flex-direction: column;
}

.contacto {
  font-size: 12px;
  line-height: 25px;
  text-transform: uppercase;
}
.icon {
  width: 100%;
  margin-right: 15px;
  cursor: pointer;
}
.icon:hover {
  transition: 0.3s;
  transform: scale(1.3);
  color: #ffa500;
}

a.enlace-redes {
  text-decoration: none;
  color: rgb(248, 247, 247);
}

.final {
  background-color: #b3b3b3;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.final__texto {
  font-size: 15px;
}
</style>