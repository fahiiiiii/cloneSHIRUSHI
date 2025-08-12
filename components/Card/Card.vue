<!-- Card.vue -->
<template>
  <v-row class="ma-0 pa-0" no-gutters>
    <v-col cols="12" sm="6" class="pa-0 pr-1 pb-1">
      <CardImage1 />
    </v-col>

    <v-col cols="12" sm="6" class="pa-0 pl-1 pb-1">
      <CardImage2 />
    </v-col>

    <v-col cols="12" sm="6" class="pa-0 pr-1 pt-1">
      <CardImage3 />
    </v-col>

    <v-col cols="12" sm="6" class="pa-0 pl-1 pt-1">
      <CardImage4 />
    </v-col>

    <v-col cols="12" sm="6" class="pa-0 pr-1 pt-1">
      <CardImage5 />
    </v-col>

    <v-col cols="12" sm="6" class="pa-0 pl-1 pt-1">
      <CardImage6 />
    </v-col>
  </v-row>
</template>

<script setup>
import CardImage1 from './CardImage1.vue'
import CardImage2 from './CardImage2.vue'
import CardImage3 from './CardImage3.vue'
import CardImage4 from './CardImage4.vue'
import CardImage5 from './CardImage5.vue'
import CardImage6 from './CardImage6.vue'
</script>

<style scoped>
/* Custom spacing for edge cards */
.v-col:first-child,
.v-col:nth-child(2) {
  padding-top: 0 !important;
}

.v-col:first-child,
.v-col:nth-child(odd) {
  padding-left: 0 !important;
}

.v-col:nth-child(2),
.v-col:nth-child(even) {
  padding-right: 0 !important;
}

.v-col:nth-last-child(1),
.v-col:nth-last-child(2) {
  padding-bottom: 0 !important;
}
</style>