<template>
  <BasicLayouts>
    <!--INICIO NOSOTROS-->
    <main class="contenedor-nosotros">

    <!-- Quienes Somos -->
      <div class="nosotros">
        <div class="nosotros__cont">
          <h2 class="nosotros__h2">¿Quiénes Somos?</h2>
          <p class="nosotros__parrafo">
            2D Store es una tienda dedicada a la venta y distribución de componentes electrónicos para equipos de computo y derivados donde sus principales ventas proveen por E-Commerce. <br /> De procedencia Colombiana cuenta con operaciones en todo el regimen nacional la cual se ha carácterizado por su gran eficiencia y calidad, la misma que le ha ayudado a obtener distintos reconocimientos en el mercado electrónico a nivel global.
            <br />
          </p>
        </div>
        <img class="nosotros__img" src="../assets/Logo_Menu.svg" />
      </div>

      <!-- Compromiso -->
      <div class="nosotros">
        <img class="nosotros__img" src="../assets/servicios-de-apoyo.svg" />
        <div class="nosotros__cont">
          <h2 class="nosotros__h2">Compromiso</h2>
          <p class="nosotros__parrafo">
           Nuestro compromiso de servicio contigo implica una estrategia personalizada para tu empresa, con el conocimiento experto y la experiencia necesaria para desarrollar, orientación y ajuste de tus planes a medida que tu compañía evoluciona. <br/>
          </p>
        </div>
      </div>

      <!-- Calidad de Servicio -->
      <div class="nosotros">
        <div class="nosotros__cont">
          <h2 class="nosotros__h2">Calidad de Servicio</h2>
          <p class="nosotros__parrafo">
           Trabajamos junto a ti y te proporcionamos un claro estándar de lo que puedes esperar de nosotros, lo que brinda transparencia al proceso y a las soluciones que te ofrecemos.  <br />
          </p>
        </div>
        <img class="nosotros__img" src="../assets/calidad.svg" />
      </div>

      <!-- Experiencia -->
      <div class="nosotros">
        <img class="nosotros__img" src="../assets/experiencia.svg" />
        <div class="nosotros__cont">
          <h2 class="nosotros__h2">Experiencia</h2>
          <p class="nosotros__parrafo">
           2 años de trabajo honesto nos posicionán como una de las mejores tiendas, tanto a nivel local como nacional, por esta razón nos sentimos comprometidos día a día con nuestros clientes. <br/>
          </p>
        </div>
      </div>

      <!-- Satisfacción -->
      <div class="nosotros">
        <div class="nosotros__cont">
          <h2 class="nosotros__h2">Satisfacción</h2>
          <p class="nosotros__parrafo">
           Nuestro principal objetivo es que usted se sienta seguro al contratar los servicios de 2D STORE. Si, por alguna razón, no está satisfecho con los servicios, nosotros tampoco lo estamos.  <br />
          </p>
        </div>
        <img class="nosotros__img" src="../assets/satisfaccion.svg" />
      </div>


      <div class="nosotros__team">
        <h2 class="title">Nuestro Equipo de Trabajo</h2>
        <div class="nosotros__team-container">
          <div class="nosotros__team-cont nosotros__team-cont--oscar">
            <img
              class="nosotros__team-img"
              src="../assets/oscar.jpg"
              alt="img"
            />

            <div class="nosotros__team-info">
              <h3 class="nosotros__nombre">Mauricio Sánchez Abella</h3>
              <div class="nosotros__team-redes">
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="facebook square icon"></i>
                </a>
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="instagram icon"></i>
                </a>
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="twitter icon"></i>
                </a>
              </div>
              <p class="nosotros__parrafo">
                Ingeniero de Sistemas y Desarrollador de Software egresado de
                la Universidad del Cauca. Es amante y aficionado por la fotografía de naturaleza.
              </p>
            </div>
          </div>
          <div class="nosotros__team-cont nosotros__team-cont--julian">
            <img
              class="nosotros__team-img"
              src="../assets/JUlian.jpg"
              alt="img"
            />
            <div class="nosotros__team-info">
              <h3 class="nosotros__nombre">Jhonatan Castillo Quevedo</h3>
              <div class="nosotros__team-redes">
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="facebook square icon"></i>
                </a>
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="instagram icon"></i>
                </a>
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="twitter icon"></i>
                </a>
              </div>
              <p class="nosotros__parrafo">
                Ingeniero de Sistemas y Desarrollador de Software egresado de
                la Universidad del Cauca. Es amante y aficionado por la fotografía de naturaleza.
              </p>
            </div>
          </div>

          <div class="nosotros__team-cont nosotros__team-cont--michael">
            <img
              class="nosotros__team-img"
              src="../assets/David.jpg"
              alt="img"
            />
            <div class="nosotros__team-info">
              <h3 class="nosotros__nombre">David Andrés García Peña</h3>
              <div class="nosotros__team-redes">
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="facebook square icon"></i>
                </a>
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="instagram icon"></i>
                </a>
                <a
                  class="enlace-redes-team"
                  href="#"
                >
                  <i class="twitter icon"></i>
                </a>
              </div>
              <p class="nosotros__parrafo">
                Ingeniero de Sistemas y Desarrollador de Software egresado de
                la Universidad del Cauca. Es amante y aficionado por la fotografía de naturaleza.
              </p>
            </div>
          </div>
        </div>
      </div>
    </main>

    <!--FIN NOSOTROS-->
  </BasicLayouts>
</template>

<script>
import BasicLayouts from "../layouts/BasicLayouts.vue";
export default {
    components: { BasicLayouts },
    name: "Nosotros",
}
</script>

<style  lang="scss" scoped>
/*INICIO PAGINA NOSOTROS**/

.contenedor-nosotros {
  max-width: 100%;
  width: 95%;
  margin: 0 auto;
  padding-bottom: 2rem;
}

.nosotros__cont {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 100%;
}

.nosotros__h2 {
  font-size: 2rem;
  text-align: center;
}

h3 {
  font-size: 1.8rem;
}

h2.title{
    text-align: center;
    font-size: 2.3rem;
    padding: 10px;
}

@media (min-width: 750px) {
  .nosotros {
    width: 100%;
    margin: 0 auto 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
    margin-bottom: 1.5rem;
    align-items: center;
    border-radius: 2rem;
    padding: 1rem;
  }
}

.nosotros {
  margin-bottom: 0.5rem;
}
.nosotros__img {
  height: 10rem;
  border-radius: 1rem;
  width: 100%;
  margin-top: 0.5rem;
}

.nosotros__team {
  padding: 1rem 0;
}
.nosotros__team-container {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}
.nosotros__team-cont {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
  width: 24rem;
  min-height: auto;
  box-shadow: 0 12px 16px rgba(0, 0, 0, 0.2);
  border-radius: 0.4rem;
  background: #f3d9ce; /* fallback for old browsers */
  background: linear-gradient(
    to right,
    #ffffff,
    #f3d9ce
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
.nosotros__nombre {
  text-align: center;
  padding: 25px;
  padding-bottom: 8px;
}
.nosotros__team-info {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}
.nosotros__team-redes {
  text-align: center;
}
.nosotros__parrafo {
  text-align: justify;
  padding: 8px;
}
.nosotros__team-img {
  width: 10rem;
  height: 10rem;
  border-radius: 50%;
  box-shadow: 0 0.75rem 1rem rgba(0, 0, 0, 0.2);
}

a.enlace-redes-team {
  text-decoration: none;
  color: black;
}
/*FIN PAGINA NOSOTROS**/
</style>