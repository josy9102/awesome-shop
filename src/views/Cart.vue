<template>
  <v-container>
    <v-row>
      <v-col class="col-12" sm="8" md="5" offset-md="2" lg="4" offset-lg="3">
        <ProductList />
      </v-col>
      <v-col class="col-12" sm="4" md="3" order="first" order-sm="last">
        <CheckoutBox />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ProductList from '@/components/cart/ProductList.vue'
import CheckoutBox from '@/components/cart/CheckoutBox.vue'

export default {
  components: {
    ProductList,
    CheckoutBox
  }
}
</script>
