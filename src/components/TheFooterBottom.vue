<script>
export default {
    name: "TheFooterBottom",
    data() {
        return {
            iconList: [
                {
                    type: 'fa-brands',
                    icon: 'facebook-f'
                },
                {
                    type: 'fa-brands',
                    icon: 'twitter'
                },
                {
                    type: 'fa-brands',
                    icon: 'youtube'
                },
                {
                    type: 'fa-brands',
                    icon: 'pinterest-p'
                },
                {
                    type: 'fa-solid',
                    icon: 'location-dot'
                }
            ]
        }
    }
}
</script>

<template>
    <section id="footer-bottom">
        <div class="bg-size">
            <div class="container display">
                <button>SIGN-UP NOW!</button>
                <ul>
                    <li>
                        <h3>
                            FOLLOW US
                        </h3>
                    </li>
                    <li v-for="element in iconList">
                        <div class="circle">
                            <i :class="['fa-' + element.icon, element.type]"></i>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>
  
<style lang="scss" scoped>
@use '../styles/partials/variables';
@use '../styles/partials/mixins';

#footer-bottom {
    background-color: variables.$color-secondary;
    height: 20%;
    width: 100%;
}

.bg-size {
    background-color: variables.$color-footer;
    height: 70%;
}

.display {
    @include mixins.d-flex-between;
    height: 100%;
}

button {
    padding: 1rem;
    border: 3px solid variables.$color-primary;
    background-color: transparent;
    color: variables.$color-white;
    font-weight: bold;
    font-size: 18px;
    cursor: pointer;
}

button:hover {
    background-color: variables.$color-white;
    color: variables.$color-black;
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

h3 {
    color: variables.$color-primary;

}

li {
    display: inline-block;
    padding: 10px;
}
</style>