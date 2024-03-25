<template>
    <div class="product-card">
        <div class="product-image">
            <img :src="product.imageSrc" alt="">
        </div>
        <div class="product-content">
            <h2>{{ product.name }}</h2>
            <p>{{ product.description }}</p>
            <div class="product-price">{{ product.price }}</div>
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
.product-card {
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 10px;
    margin-bottom: 20px;
}

.product-image img {
    width: 100%;
    border-radius: 5px;
}

.product-content {
    padding-top: 10px;
}

.product-content h2 {
    font-size: 1.2em;
}

.product-content p {
    font-size: 0.8em;
}

.product-price {
    font-weight: bold;
    font-size: 1.1em;
    color: #007bff;
}
</style>