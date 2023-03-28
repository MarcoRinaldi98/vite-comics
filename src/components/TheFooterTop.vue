<script>
export default {
    name: "TheFooterTop",
    props: {
        image: Array
    }, methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}

</script>

<template>
    <section id="footer-top">
        <div class="container display">
            <div class="box" v-for="(element, index) in image">
                <img :src="getImagePath(element.image)" :key="index" />
                <span>
                    <a href="#">
                        {{ element.text }}
                    </a>
                </span>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#footer-top {
    background-color: #0282f9;
    height: 30%;
    width: 100%;

    .container {
        @include mixins.contenitore;
        @include mixins.d-flex-around;
        height: 100%;
        padding: 0 20px;

        .box {
            height: 80px;
            @include mixins.d-flex-center;

            img {
                height: 100%;
            }

            span {
                text-decoration: none;
                text-transform: uppercase;
                font-size: 14px;
                margin-left: 10px;
                font-weight: 600;
            }

            a {
                text-decoration: none;
                color: variables.$color-white;

                &:hover {
                    text-decoration: underline;
                }
            }

            &:last-child img {
                height: 70%;
            }
        }
    }
}
</style>