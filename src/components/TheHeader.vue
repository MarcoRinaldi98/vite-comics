<script>
export default {
    name: "TheHeader",
    data() {
        return {
            navLinks: [
                {
                    href: "#characters",
                    text: "characters"
                },
                {
                    href: "#comics",
                    text: "comics"
                },
                {
                    href: "#movies",
                    text: "movies"
                },
                {
                    href: "#tv",
                    text: "tv"
                },
                {
                    href: "#games",
                    text: "games"
                },
                {
                    href: "#collectibles",
                    text: "collectibles"
                },
                {
                    href: "#videos",
                    text: "videos"
                },
                {
                    href: "#fans",
                    text: "fans"
                },
                {
                    href: "#news",
                    text: "news"
                },
                {
                    href: "#shop",
                    text: "shop"
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <nav>
            <div class="brand">
                <a href="#">
                    <img src="../assets/dc-logo.png" />
                </a>
            </div>
            <ul class="navbar-link">
                <li v-for="(link, i) in navLinks" :key="i">
                    <a class="nav-link" :href="link.href">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

header {
    background-color: variables.$color-white;
    height: 100%;
    width: 100%;

    .brand {
        height: 100%;

        img {
            width: calc(100% - 20px);
            padding: 10px;
        }
    }

    nav {
        @include mixins.contenitore;
        @include mixins.d-flex-between;
        height: 100%;

        ul {
            height: 100%;

            li {
                height: 100%;
                display: inline-block;
                line-height: 100px;

                &:hover {
                    border-bottom: 4px solid variables.$color-primary;
                }

                .nav-link {
                    text-decoration: none;
                    padding: 10px;
                    text-transform: uppercase;
                    font-size: 12px;
                    font-weight: bold;
                    color: variables.$color-black;
                }

                &:hover .nav-link {
                    color: variables.$color-primary;
                }
            }
        }
    }
}
</style>