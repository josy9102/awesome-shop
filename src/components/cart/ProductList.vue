<template>
  <div>
    <v-row v-for="(product, i) in products" :key="i" class="ma-0">
      <HorizontalProduct
        :product="product"
        :i="i"
        :updateCart="removeFromCart"
        btnAction="remove"
      />
    </v-row>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import HorizontalProduct from '@/components/cards/HorizontalProduct.vue'

export default {
  components: {
    HorizontalProduct
  },
  data() {
    return {}
  },
  computed: {
    ...mapState(['products'])
  },
  methods: {
    removeFromCart() {
    }
  }
}
</script>
