<template>
  <div>
    <v-app-bar
      :elevation="showContent ? 5 : 0"
      class="px-4 transition-all"
      @mouseenter="showContent = true"
      @mouseleave="checkScroll"
    >
      <!-- Left: Logo -->
      <template v-slot:prepend>
        <a href="/">
          <img
            src="/shirushi-logo.png"
            alt="Logo"
            style="height: 40px; cursor: pointer;"
          />
        </a>
      </template>

      <!-- Center: Nav Buttons -->
      <v-toolbar-items
        class="mx-auto d-flex gap-4"
        v-show="showContent"
      >
        <v-btn variant="text" class="nav-middle-part">Company Information</v-btn>
        <v-btn variant="text" class="nav-middle-part">Business Content</v-btn>
        <v-btn variant="text" class="nav-middle-part">Inquiry</v-btn>
        <v-btn variant="text" class="nav-middle-part">Web3 Maker Login</v-btn>
        <v-btn variant="text" class="nav-middle-part">Recruitment Information</v-btn>
        <v-btn variant="text" class="nav-middle-part">English</v-btn>
      </v-toolbar-items>

      <!-- Right: Search Icon -->
      <template v-slot:append v-if="showContent">
        <v-btn icon @click="onSearch">
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </template>
    </v-app-bar>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const showContent = ref(false);

function onSearch() {
  alert('Search clicked!');
}

function checkScroll() {
  if (window.scrollY > 0) {
    showContent.value = true;
  } else {
    showContent.value = false;
  }
}

function handleScroll() {
  if (window.scrollY > 0) {
    showContent.value = true;
  } else {
    showContent.value = false;
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.gap-4 > * + * {
  margin-left: 1rem;
}

.nav-middle-part {
  font-size: 14px;
}

.transition-all {
  transition: all 0.3s ease-in-out;
}
</style>
