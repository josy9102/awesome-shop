<template>
  <div>
    <v-sheet :height="sheetHeight">
      <v-container class="fill-height">
        <v-row align="center" justify="center">
          <h1 class="text-center" :class="h1Size">Welcome to the Awesome Shop!</h1>
        </v-row>
      </v-container>
    </v-sheet>
  </div>
</template>

<script>
export default {
  computed: {
    sheetHeight() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return "200px";
        case "sm":
          return "300px";
        case "md":
          return "300px";
        case "lg":
          return "300px";
        case "xl":
          return "350px";
      }
      return "300px";
    },
    h1Size() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return "display-1";
      }
      return "display-3";
    }
  },
};
</script>
