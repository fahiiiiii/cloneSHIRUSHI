<template>
  <div class="section-wrapper">
    <v-card class="custom-card">
      <v-card-item>
        <v-card-title class="custom-title">
          サービス
        </v-card-title>
        <v-card-subtitle class="custom-text subtitle">
          SERVICE
        </v-card-subtitle>
      </v-card-item>

      <v-card-text class="custom-text">
        <p>Web3専門の半導体メーカーとして</p>
        <p>あらゆるモノにブロックチェーンを導入し、日本製品を再び世界の舞台に！</p>
      </v-card-text>
      <Card/>
    </v-card>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.section-wrapper {
  display: flex;
  justify-content: center;
  /* center horizontally */
  margin-top: 100px;
  /* space from top */
}

.custom-card {
  border-left: 1px solid rgb(221, 221, 221);
  border-right: 1px solid rgb(221, 221, 221);
  border-bottom: 1px solid rgb(221, 221, 221);
  font-weight: 400;
  // elevation: 0;
  box-shadow: none;
  /* removes Vuetify shadow */
  max-width: 60%;
  width: 100%;
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;

}

.custom-title {
  font-weight: 600;
  font-size: 36px;
  color: #001A43;
  padding-top: 70px;

}
.custom-text{
  text-align: center;
  font-weight: 400;
  font-size: 14px;
  color: #212121;
  padding: 10px;

}
.subtitle{
  color: #9B9B9B;
  margin-bottom: 40px;
}
</style>
