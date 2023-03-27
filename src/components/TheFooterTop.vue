<script>
export default {
    name: "TheFooterTop",
    data() {
        return {
            imageList: [
                {
                    href: "#digitalcomics",
                    text: "digital comics",
                    image: "buy-comics-digital-comics.png"
                },
                {
                    href: "#merch",
                    text: "dc merchandise",
                    image: "buy-comics-merchandise.png"
                },
                {
                    href: "#subscription",
                    text: "subscription",
                    image: "buy-comics-subscriptions.png"
                },
                {
                    href: "#shop",
                    text: "comic shop locator",
                    image: "buy-comics-shop-locator.png"
                },
                {
                    href: "#visa",
                    text: "dc power visa",
                    image: "buy-dc-power-visa.svg"
                }
            ]
        }
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
            <div class="box" v-for="element in imageList">
                <img :src="getImagePath(element.image)" />
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
}

.display {
    @include mixins.d-flex-around;
    height: 100%;
}

.box {
    height: 60px;
    @include mixins.d-flex-center;
    padding: 0 5px;
}

img {
    height: 100%;
}

span {
    text-decoration: none;
    text-transform: uppercase;
    font-size: 14px;
    margin-left: 5px;
}

a {
    text-decoration: none;
    color: variables.$color-white;
}
</style>