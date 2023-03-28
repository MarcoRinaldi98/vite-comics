<script>
export default {
    name: "TheFooterCenter",
    props: {
        fLinks: Array
    }
}
</script>

<template>
    <section id="footer-center">
        <div class="container">
            <ul v-for="(link, i) in fLinks" :key="i">
                <li>
                    <h3>
                        {{ link.name }}
                    </h3>
                </li>
                <li v-for="element in link.type">
                    <a href="#">
                        {{ element }}
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>
   
<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#footer-center {
    background-image: url(/footer-bg.jpg);
    height: 50%;
    width: 100%;

    .container {
        @include mixins.contenitore;
        display: flex;
        height: 100%;
        background-image: url(/dc-logo-bg.png);
        background-position: right;
        background-repeat: no-repeat;

        ul {
            padding-right: 20px;
            margin-top: 10px;

            li {
                list-style: none;
                padding: 5px 0;

                h3 {
                    color: variables.$color-white;
                    font-size: 20px;
                    text-transform: uppercase;
                }

                a {
                    text-decoration: none;
                    color: variables.$color-grey;
                    font-size: 12px;

                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
    }
}
</style>