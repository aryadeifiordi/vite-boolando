<template>
  <header class="header-container">
    <ul class="choose">
      <li>Donna</li>
      <li>Uomo</li>
      <li>Bambini</li>
    </ul>

    <div class="boolean">
      <img class="img-boolean" src="/img/boolean-logo.png" alt="">
    </div>

    <div>
      <i class="fas fa-shopping-bag"></i>
      <i class="far fa-user"></i>
      <i class="far fa-heart"></i>
    </div>
  </header>
</template>

<script>
export default {

};
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