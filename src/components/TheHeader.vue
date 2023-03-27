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
        <nav class="container">
            <div class="brand">
                <img src="../assets/dc-logo.png" />
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

header {
    background-color: variables.$color-white;
    height: 100%;
    width: 100%;
}

.brand {
    height: 100%;

    img {
        width: calc(100% - 20px);
        padding: 10px;
    }
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;

    ul {
        height: 100%;

        li {
            height: 100%;
            display: inline-block;
            line-height: 100px;

            .nav-link {
                text-decoration: none;
                padding: 10px;
                text-transform: uppercase;
                font-size: 12px;
                font-weight: bold;
                color: variables.$color-black;
            }
        }
    }
}

li:hover .nav-link {
    color: variables.$color-primary;
}

li:hover {
    border-bottom: 4px solid variables.$color-primary;
}
</style>