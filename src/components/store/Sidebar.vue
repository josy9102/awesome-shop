<template>
  <div>
    <v-sheet
      height="300"
      :elevation="4"
      class="pa-8"
      v-if="$vuetify.breakpoint.mdAndUp"
    >
      <h3>Filters</h3>
      <v-radio-group v-model="priceFilter" :mandatory="true">
        <v-radio
          v-for="(price, i) in prices"
          :key="i"
          :label="price"
          :value="i"
        />
      </v-radio-group>
    </v-sheet>
    <v-expansion-panels v-else>
      <v-expansion-panel>
        <v-expansion-panel-header> <h4>Filters</h4> </v-expansion-panel-header>
        <v-expansion-panel-content>
          <v-radio-group v-model="priceFilter" :mandatory="true">
            <v-radio
              v-for="(price, i) in prices"
              :key="i"
              :label="price"
              :value="i"
            />
          </v-radio-group>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
export default {
  data() {
    return {
      prices: ["Any", "Under $25", "$25 to $100", "$100 to $500", "Over $500"],
      priceFilter: 0,
    };
  },
};
</script>
