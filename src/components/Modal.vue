<template>
    <div class="modal-overlay" @click="closeModal">
        <div class="modal">
            <div class="modal-header">
                <h2>{{ product.brand }}</h2>
                <button @click.stop="closeModal">&times;</button>
            </div>
            <div class="modal-content">
                <img class="modal-img" :src="product.imageSrc" alt="">
                <p>{{ product.title }}</p>
                <p v-if="product.discount">{{ product.discount }}</p>
                <p v-if="product.sustainability">{{ product.sustainability }}</p>
            </div>
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
    },
    methods: {
        closeModal() {
            this.$emit('closeModal');
        }
    }
};
</script>

<style scoped>
.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
}

.modal {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
}

.modal-header h2 {
    margin: 0;
}

.modal-header button {
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
}

.modal-content {
    text-align: center;
}

.modal-img {
    width: 200px;
    height: auto;
}
</style>