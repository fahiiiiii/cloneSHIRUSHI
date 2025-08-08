<template>
  <v-layout>
    <!-- Include the hamburger drawer -->
    <TopNavBar />

    <!-- Page content will appear here -->
    <v-main>
      <v-container>
        <slot />
      </v-container>
    </v-main>
  </v-layout>
</template>

<script setup>
import LayoutNavbar from '#components'

import TopNavBar from '../components/TopNav/TopNavBar.vue';
</script>