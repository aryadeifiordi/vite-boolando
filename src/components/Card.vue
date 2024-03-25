<template>
  <div class="container">
    <div class="row">
      <div class="card" v-for="(card, index) in cards.slice(0, 3)" :key="index">
        <div class="card-image">
          <img class="card-img" :src="card.imageSrc" alt="">
          <div v-if="card.discount" class="box-red">{{ card.discount }}</div>
          <div v-if="card.sustainability" class="box-green">{{ card.sustainability }}</div>
          <i class="fa-solid fa-heart card-heart"></i>
        </div>
        <div class="card-content">
          <h1>{{ card.brand }}</h1>
          <h2>{{ card.title }}</h2>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="card" v-for="(card, index) in cards.slice(3)" :key="index">
        <div class="card-image">
          <img class="card-img" :src="card.imageSrc" alt="">
          <div v-if="card.discount" class="box-red">{{ card.discount }}</div>
          <div v-if="card.sustainability" class="box-green">{{ card.sustainability }}</div>
          <i class="fa-solid fa-heart card-heart"></i>
        </div>
        <div class="card-content">
          <h1>{{ card.brand }}</h1>
          <h2>{{ card.title }}</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          brand: "Levi's",
          title: "RELAXED FIT TEE UNISEX",
          imageSrc: "/img/1.webp",
          discount: "-30%",
          sustainability: "sostenibilità",
        },
        {
          brand: "Guess",
          title: "Roses Tee",
          imageSrc: "/img/2.webp",
          discount: "-30%",
        },
        {
          brand: "Come zucchero filato",
          title: "VOGLIA DI COLORI PASTELLO",
          imageSrc: "/img/3.webp",
          discount: "-30%",
        },
        {
          brand: "Levi's",
          title: "TEE UNISEX",
          imageSrc: "/img/4.webp",
          discount: "-50%",
          sustainability: "sostenibilità",
        },
        {
          brand: "Maya Deluxe",
          title: "STRIPE BODICE",
          imageSrc: "/img/5.webp",
        },
        {
          brand: "Esprit",
          title: "MAGLIONE-BLACK",
          imageSrc: "/img/6.webp",
        },
      ]
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}

.row {
  flex: 1;
  display: flex;
  flex-direction: row;
  margin-bottom: 20px;
}

.card {
  margin-right: 20px;
  flex: 1;
}

.card:last-child {
  margin-right: 0;
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