<template>
  <div>
    <AppHeader />
    <Card v-for="product in products" :key="product.id" :product="product" />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import Card from './components/Card.vue';

export default {
  components: {
    AppHeader,
    Card,
  },
  data() {
    return {
      products: [
        {
          id: "1",
          brand: "Levi's",
          title: "RELAXED FIT TEE UNISEX",
          imageSrc: "/img/1.webp",
          discount: "-30%",
          sustainability: "sostenibilità",
        },
        {
          id: "2",
          brand: "Guess",
          title: "Roses Tee",
          imageSrc: "/img/2.webp",
          discount: "-30%",
        },
        {
          id: "3",
          brand: "Come zucchero filato",
          title: "VOGLIA DI COLORI PASTELLO",
          imageSrc: "/img/3.webp",
          discount: "-30%",
        },
        {
          id: "4",
          brand: "Levi's",
          title: "TEE UNISEX",
          imageSrc: "/img/4.webp",
          discount: "-50%",
          sustainability: "sostenibilità",
        },
        {
          id: "5",
          brand: "Maya Deluxe",
          title: "STRIPE BODICE",
          imageSrc: "/img/5.webp",
        },
        {
          id: "6",
          brand: "Esprit",
          title: "MAGLIONE-BLACK",
          imageSrc: "/img/6.webp",
        },
      ],
    };
  },
};
</script>

<style scoped></style>