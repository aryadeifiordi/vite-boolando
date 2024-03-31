<template>
  <div class="product-grid">
    <AppHeader />
    <div class="grid-container">
      <Card v-for="product in products" :key="product.id" :product="product" @showModal="openModal" />
    </div>
    <Modal :product="selectedProduct" v-if="modalOpened" @closeModal="closeModal" />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import Card from './components/Card.vue';
import Modal from './components/Modal.vue';

export default {
  components: {
    AppHeader,
    Card,
    Modal
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
          category: "Donna"
        },
        {
          id: "2",
          brand: "Guess",
          title: "Roses Tee",
          imageSrc: "/img/2.webp",
          discount: "-30%",
          category: "Donna"
        },
        {
          id: "3",
          brand: "Come zucchero filato",
          title: "VOGLIA DI COLORI PASTELLO",
          imageSrc: "/img/3.webp",
          discount: "-30%",
          category: "Donna"
        },
        {
          id: "4",
          brand: "Levi's",
          title: "TEE UNISEX",
          imageSrc: "/img/4.webp",
          discount: "-50%",
          sustainability: "sostenibilità",
          category: "Uomo"
        },
        {
          id: "5",
          brand: "Maya Deluxe",
          title: "STRIPE BODICE",
          imageSrc: "/img/5.webp",
          category: "Uomo"
        },
        {
          id: "6",
          brand: "Esprit",
          title: "MAGLIONE-BLACK",
          imageSrc: "/img/6.webp",
          category: "Bambini"
        },

      ],
      modalOpened: false,
      selectedProduct: null
    };
  },
  methods: {
    openModal(product) {
      this.modalOpened = true;
      this.selectedProduct = product;
    },
    closeModal() {
      this.modalOpened = false;
    }
  }
};
</script>

<style scoped>
.product-grid {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  justify-content: center;
}

.grid-container .card {
  width: 100%;
  margin: 0 auto;
}
</style>