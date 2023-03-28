<script>
export default {
    name: "TheHero"
}
</script>

<template>
    <section id="jumbotron">
        <div class="container">
            <span class="title">
                CURRENT SERIES
            </span>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#jumbotron {
    height: 450px;
    background-image: url(/jumbotron.jpg);
    background-size: cover;
    background-repeat: no-repeat;

    .container {
        @include mixins.contenitore;
        height: 100%;
        position: relative;

        .title {
            background-color: variables.$color-primary;
            padding: 1rem 3rem;
            position: absolute;
            left: 0;
            bottom: -1.5rem;
            color: variables.$color-white;
            font-weight: bolder;
            font-size: 20px;
        }
    }
}
</style>