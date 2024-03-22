<template>
    <div class="card">
      <div class="card-image">
        <img class="card-img" :src="imageSrc" alt="">
        <div v-if="discount" class="box-red">{{ discount }}</div>
        <div v-if="sustainability" class="box-green">{{ sustainability }}</div>
        <i class="fa-solid fa-heart card-heart"></i>
      </div>
      <div class="card-content">
        <h1>{{ brand }}</h1>
        <h2>{{ title }}</h2>
      </div>
    </div>
  </template>
  
  <script>
  const brand = 'Levi\'s';
  const title = 'RELAXED FIT TEE UNISEX';
  const imageSrc = '/img/1.webp'; 
  const discount = '-30%';
  const sustainability = 'sostenibilità'; 
  </script>
  
  <style scoped>
  .card {
    width: calc(100% / 3);
    align-content: center;
    overflow: hidden;
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
    width: 40px;
    height: 20px;
    position: absolute;
    bottom: 10px;
    display: flex;
    justify-content: space-around;
  }
  
  .box-red {
    background-color: red;
    width: 40px;
    height: 20px;
    position: absolute;
    bottom: 10px;
    display: flex;
    align-items: center;
  }
  </style>