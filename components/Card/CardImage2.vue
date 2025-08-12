<template>
  <div>
    <v-card class="ma-0 pa-0 custom-card" max-width="100vw">
      <div class="image-wrapper">
        <v-img 
          class="align-end image"
          height="320"
          src="./../../assets/hero/web3Maker.jpeg"
          cover
        >
        </v-img>
        <div class="gradient-overlay"></div>
        <v-card-title class="card-title text-white">
          Web3 Maker® 5.0
        </v-card-title>
      </div>

      <v-card-text>
        <p>しるし製マイニングマシン「Web3Maker®」は、超省エネ＆極小です。</p>
        <p>経費で買えるのに、このリターンは革命的です。</p>
      </v-card-text>
    </v-card>
  </div>
</template>

<style lang="scss" scoped>
.card-title {
  font-weight: 600;
  color: #FFFFFF !important;
  font-size: 20px;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 3; /* Highest z-index to stay above everything */
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  transition: none; /* Prevents title from scaling */
}

.image-wrapper {
  position: relative;
  overflow: hidden; /* This is key - prevents image from breaking boundaries */
  height: 320px;
}

.gradient-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 50%;
  background: linear-gradient(to top, rgba(124, 124, 124, 0.8), transparent);
  pointer-events: none;
  z-index: 2;
  transition: none; /* Prevents overlay from scaling */
}

.image {
  transition: transform 0.3s ease; /* Smoother, faster transition */
}

.image:hover {
  transform: scale(1.5); /* Use transform instead of scale property */
}
</style>