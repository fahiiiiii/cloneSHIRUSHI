<template>
  <div>
    <v-app-bar :elevation="showContent ? 5 : 0" class="px-4 transition-all" @mouseenter="showContent = true"
      @mouseleave="checkScroll">
      <!-- Logo -->
      <template v-slot:prepend>
        <a href="/">
          <img src="/shirushi-logo.png" alt="Logo" style="height: 40px; cursor: pointer;" />
        </a>
      </template>

      <!-- Center: Nav Buttons -->
      <v-toolbar-items class="mx-auto d-flex gap-4" v-if="showContent">

        <v-btn variant="text" class="nav-middle-part">企業情報</v-btn>
        <v-btn variant="text" class="nav-middle-part">事業内容</v-btn>
        <v-btn variant="text" class="nav-middle-part">お問い合わせ</v-btn>
        <v-btn variant="text" class="nav-middle-part">Web3 Maker ログイン</v-btn>
        <v-btn variant="text" class="nav-middle-part">採用情報</v-btn>
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

const showContent = ref(false); // stays false on load

function onSearch() {
  alert('Search clicked!');
}

function checkScroll() {
  // only show if actually scrolled down
  if (window.scrollY > 0) {
    showContent.value = true;
  } else {
    showContent.value = false;
  }
}

function handleScroll() {
  checkScroll();
}

onMounted(() => {
  // Don't trigger showContent on load
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>


<style scoped>
.gap-4>*+* {
  margin-left: 1rem;
}

.nav-middle-part {
  font-weight: 800;
  font-size: 14px;
}

.transition-all {
  transition: all 0.3s ease-in-out;
}
</style>
