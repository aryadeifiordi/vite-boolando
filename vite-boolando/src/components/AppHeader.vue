<template>
    <header class="header-container">
      <ul class="choose">
        <li>Donna</li>
        <li>Uomo</li>
        <li>Bambini</li>
      </ul>
  
      <div class="boolean">
        <img class="img-boolean" src="assets/img/img/boolean-logo.png" alt="">
      </div>
  
      <div>
        <i class="fa-solid fa-bag-shopping"></i>
        <i class="fa-regular fa-user"></i>
        <i class="fa-regular fa-heart"></i>
      </div>
    </header>
  </template>
  
  <script setup>
  
  </script>
  
  <style scoped>
  .header-container {
    background-color: #ff5b00;
    width: auto;
    height: 50px;
    display: flex;
    justify-content: space-between;
  }
  
  .choose {
    list-style-type: none;
    display: flex;
    justify-content: space-between;
    gap: 0.5rem;
  }
  
  .img-boolean {
    width: 120px;
  }
  
  .boolean {
    display: flex;
    align-items: center;
  }
  
  .header-container i {
    font-size: 30px;
    color: white;
  }
  </style>