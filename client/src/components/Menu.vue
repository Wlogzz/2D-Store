<template>
  <div class="ui secondary menu">
    <div class="contenedor">
      <div class="menu-container">
        <div class="logo-container">
          <router-link class="" to="/">
          <img class="logo" src="../assets/Logo_Menu.svg" />
          </router-link>
        </div>

        <div id="menu">
          <ul>
            <li>
              <router-link class="item" to="/">
                2D Store
              </router-link>
            </li>

            <li>
              <router-link class="item" to="/productos">
                Productos
              </router-link>
              <ul>
                <li v-for="category in categories" :key="category.id">
                  <router-link class="item" :to="category.slug">
                    <!-- {{ category.title }} -->
                  </router-link>
                </li>
              </ul>
            </li>

            <li>
              <router-link class="item" to="/nosotros">
                Nosotros
              </router-link>
            </li>

            <li>
              <router-link class="item" to="/login" v-if="!token">
                Iniciar Sesión</router-link
              >
            </li>

            <template v-if="token">
              <li>
                <router-link class="item" to="/Cart">Pedidos</router-link>
              </li>

              <li>
                <span class="ui item cart" @click="openCart">
                  <i class="shopping cart icon"></i>
                </span>
              </li>

              <li>
                <span class="ui item logout" @click="logout">
                  <i class="sign-out icon"></i>
                </span>
              </li>
            </template>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useStore } from 'vuex';
import { getTokenApi, deleteTokenApi } from '../api/token';
import { getCategoriesApi } from '../api/category';

export default {
  name: 'Menu',

  setup() {
    let categories = ref(null);
    const token = getTokenApi();
    const store = useStore();

    onMounted(async () => {
      const response = await getCategoriesApi();
      categories.value = response;
    });

    const logout = () => {
      deleteTokenApi();
      location.replace('/');
    };

    const openCart = () => {
      store.commit('setShowCart', true);
    };

    return {
      token,
      logout,
      categories,
      openCart,
    };
  },
};
</script>

<style lang="scss" scoped>
.ui.menu.secondary {
  background-color: #16202b;
  .item {
    color: #ffffff;
    &:hover {
    color: #ffa500;
      
    }
  }
}

p {
  font-size: 20px;
  text-align: center;
}

h1 {
  font-size: 50px;
  margin: 0;
  color: #222222;
}

.header-section {
  margin-bottom: 50px;
}

.contenedor {
  width: 100%;
  margin: auto;
}

.logo-container {
  width: 10%;
  text-align: right;
  margin-bottom: 2%;
}
.logo-container h2 {
  margin-top: 1%;
}
.logo {
  height: 100px;
}

.menu-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

/* menu */

#menu {
  width: 30%;
}

#menu ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

/* items del menu */

#menu ul li {
  position: relative;
  float: left;
  margin: auto;
  padding: auto;
}

/* menu desplegable */

#menu ul ul {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  // background: #eee;
  padding: 0;
}

/* items del menu desplegable */

#menu ul ul li {
  float: none;
  width: 150px;
}

/* enlaces de los items del menu desplegable */

#menu ul ul a {
  line-height: 120%;
  padding: 10px 15px;
}

/* items del menu desplegable al pasar el ratón */

#menu ul li:hover > ul {
  display: block;
}
</style>
