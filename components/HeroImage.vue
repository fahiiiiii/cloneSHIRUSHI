<template>
  <!-- Add top-bottom spacing with no horizontal padding -->
  <v-container class="pt-10 pb-10 px-0" fluid>
    <!-- Full width image with no border-radius -->
    <v-img
      src="/web3.png"
      cover
      class="rounded-0 full-width-image"
      alt="Web3.0 Semiconductor Manufacturing, Sales and Research Mark Co., Ltd."
    />
  </v-container>
</template>

<script setup>
</script>

<style scoped>
.full-width-image {
  margin-left: 0;
  padding-left: 0;
  width: 100%; /* Full width of the screen */
}
</style>
