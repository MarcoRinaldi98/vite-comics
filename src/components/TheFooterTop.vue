<script>
export default {
    name: "TheFooterTop",
    data() {
        return {
            navLinks: [
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
    }
}
</script>

<template>
    <section id="footer-top">
        <div class="container">

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';

#footer-top {
    background-color: #0282f9;
    height: 30%;
    width: 100%;
}
</style>