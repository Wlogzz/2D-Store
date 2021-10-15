<template>
  <BasicLayouts>
    <div class="title">
      <h1>Resumen de la Compra</h1>
    </div>
    <table class="ui celled table" v-if="products">
      <thead>
        <tr>
          <th>Producto</th>
          <th>Cantidad</th>
          <th>Precio</th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.id">
          <td>{{ product.name }}</td>
          <td>{{ product.quantity }}</td>
          <td>$ {{ product.price }}</td>
          <td style="text-align: center">
            <i class="close icon" @click="deleteAllProductCart(product.id)"></i>
          </td>
        </tr>
        <tr>
          <td></td>
          <td>Total:</td>
          <td colspan="2">$ {{ getTotal() }}</td>
        </tr>
      </tbody>
    </table>

    <!-- <button class="ui button orange fluid" >Generar pedido</button> -->
    
    <a href="https://api.whatsapp.com/send?phone=573202523572&text=Hola!%20Me%20comunico%20contigo%20porque%20deseo%20adquirir%20unos%20de%20tus%20productos%20de%20tu%20tienda%20virtual%202D%20Store." target="_blank" class="ui button orange fluid">Generar Pedido</a>

    <h3 v-if="!products">No tienes productos en el carrito</h3>
  </BasicLayouts>
</template>

<script>
import { ref,watchEffect } from 'vue';
import BasicLayouts from '../layouts/BasicLayouts.vue';
import { getProductsCartApi, deleteAllProductCartApi } from '../api/cart';

export default {
  name: 'Cart',
  components: {
    BasicLayouts,
  },
  setup() {
    let products = ref(null);
    let realoadCart = ref(false);

    watchEffect(async () => {
      realoadCart.value;
      const response = await getProductsCartApi();
      products.value = response;
    });

    const getTotal = () => {
      let totalTemp = 0;
      products.value.forEach((product) => {
        totalTemp += product.price * product.quantity;
      });
      return totalTemp.toFixed(2);
    };

    const deleteAllProductCart = (idProduct) => {
      deleteAllProductCartApi(idProduct);
      realoadCart.value = !realoadCart.value;
    };

    return {
      products,
      getTotal,
      deleteAllProductCart,
    };
  },
};
</script>

<style>
.title h1{
  text-align: center;
  padding-block-end: 5%;
  font-size: 3em;
}
</style>