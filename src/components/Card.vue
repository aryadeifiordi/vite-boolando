<template>
  <div class="card">
    <div class="card-image">
      <img class="card-img" :src="product.imageSrc" alt="">
      <div v-if="product.discount" class="box-red">{{ product.discount }}</div>
      <div v-if="product.sustainability" class="box-green">{{ product.sustainability }}</div>
      <i class="fa-solid fa-heart card-heart"></i>
    </div>
    <div class="card-content">
      <h1>{{ product.brand }}</h1>
      <h2>{{ product.title }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  }
};
</script>

<style scoped>
.card {
  margin-right: 20px;
  flex: 1;
}

.card-image {
  position: relative;
  padding: 1rem;
}

.card-image img {
  width: 100%;
}

.card-content h1 {
  font-size: 1.2em;
}

.card-content h2 {
  font-size: 0.5em;
}

.card .card-heart {
  color: red;
  position: absolute;
  top: 10px;
  right: 10px;
}

.box-green {
  background-color: green;
  width: fit-content;
  height: 20px;
  position: absolute;
  bottom: 10px;
  display: flex;
  align-items: center;
  padding: 0 5px;
}

.box-red {
  background-color: red;
  width: fit-content;
  height: 20px;
  position: absolute;
  bottom: 10px;
  display: flex;
  align-items: center;
  padding: 0 5px;
}
</style>