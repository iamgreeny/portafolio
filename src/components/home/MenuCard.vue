<script setup>
const props = defineProps({
  product: Object,
});
</script>

<template>
  <div class="card">
    <img :src="product.image_url" alt="" />
    <div class="container-text">
      <h1 class="title">:{{ product.name }}:</h1>
      <h3 class="description">{{ product.description }}</h3>
      <h4 class="price">{{ product.price }}</h4>
    </div>
  </div>
  <div class="borde-gris"></div>
</template>

<style scoped>
img {
  object-fit: cover;
  width: 145px;
  height: 148px;
  border-radius: 108px;
}

.card {
  background-color: rgb(255, 255, 255);
  position: relative;
  width: 260px;
  height: 330px;
  border-radius: 50px;
  border: 4px solid rgb(68, 40, 7);
  z-index: 2;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}

.borde-gris {
  display: none;
  background-color: grey;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 316px;
  height: 405px;
  border-radius: 50px;
  z-index: 1;
}
.container-text {
  text-align: center;

  width: 80%;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.title {
  font-size: 19px;
  font-family: "Times New Roman", Times, serif;
  font-weight: bold;
}

.description {
  font-size: 16px;
  color: brown;
}

.price {
  font-size: 15px;
  color: green;
  align-self: end;
}
</style>
