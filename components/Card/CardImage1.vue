<template>
  <div class="card-container">
    <div class="image-wrapper">
      <v-img 
        class="align-end image"
        height="320"
        src="./../../assets/hero/web3Maker.jpeg"
        cover
      >
      </v-img>
      <div class="gradient-overlay"></div>
      <div class="card-title text-white">
        Web3 Maker® 5.0
      </div>
    </div>

    <div class="card-content">
      <p>しるし製マイニングマシン「Web3Maker®」は、超省エネ＆極小です。</p>
      <p>経費で買えるのに、このリターンは革命的です。</p>
    </div>
  </div> 
</template>

<style lang="scss" scoped>
.card-container {
  width: 100%;
  background: white;
  overflow: hidden;
}

.card-title {
  font-weight: 600;
  color: #FFFFFF !important;
  font-size: 20px;
  position: absolute;
  bottom: 16px;
  left: 16px;
  right: 16px;
  z-index: 3;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  transition: none;
}

.image-wrapper {
  position: relative;
  overflow: hidden;
  height: 320px;
  width: 100%;
  margin: 0;
  padding: 0;
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
  transition: none;
}

.image {
  transition: transform 0.3s ease;
  width: 100%;
  height: 100%;
  display: block;
}

.image:hover {
  transform: scale(1.5);
}

.card-content {
  padding: 16px;
  background: white;
}

.card-content p {
  margin-bottom: 8px;
  line-height: 1.5;
}

.card-content p:last-child {
  margin-bottom: 0;
}
</style>