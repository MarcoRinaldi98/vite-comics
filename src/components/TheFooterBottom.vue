<script>
export default {
    name: "TheFooterBottom",
    props: {
        icon: Array
    }
}
</script>

<template>
    <section id="footer-bottom">
        <div class="container">
            <button>SIGN-UP NOW!</button>
            <ul>
                <li>
                    <h3>
                        FOLLOW US
                    </h3>
                </li>
                <li v-for="element in icon">
                    <div class="circle">
                        <i :class="['fa-' + element.icon, element.type]"></i>
                    </div>
                </li>
            </ul>
        </div>
        <div class="bottom">

        </div>
    </section>
</template>
  
<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#footer-bottom {
    background-color: variables.$color-footer;
    height: 20%;
    width: 100%;

    .container {
        background-color: variables.$color-footer;
        @include mixins.contenitore;
        @include mixins.d-flex-between;
        height: 70%;

        button {
            padding: 1rem;
            border: 3px solid variables.$color-primary;
            background-color: transparent;
            color: variables.$color-white;
            font-weight: bold;
            font-size: 18px;
            cursor: pointer;

            &:hover {
                background-color: variables.$color-white;
                color: variables.$color-black;
            }
        }

        li {
            display: inline-block;
            padding: 10px;

            h3 {
                color: variables.$color-primary;
            }

            .circle {
                height: 50px;
                width: 50px;
                background-color: variables.$color-white;
                border-radius: 50%;
                @include mixins.d-flex-center;
                font-size: 30px;
                opacity: 0.5;
                cursor: pointer;

                &:hover {
                    opacity: 1;
                }
            }
        }
    }

    .bottom {
        background-color: variables.$color-secondary;
        width: 100%;
        height: 30%;
    }
}
</style>