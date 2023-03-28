<script>
export default {
    name: "ProductCard",
    props: {
        img: String,
        name: String
    }
}
</script>

<template>
    <section id="movies">
        <div class="product-card">
            <img :src="img" :alt="name">
            <h3>{{ name }}</h3>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

.product-card {
    width: 100%;

    & img {
        width: 100%;
        height: 200px;
    }

    & h3 {
        padding-top: 1rem;
        text-transform: uppercase;
        color: variables.$color-white;
        font-weight: 200;
        font-size: 14px;
    }

    &:hover h3 {
        text-decoration: underline;
    }
}
</style>