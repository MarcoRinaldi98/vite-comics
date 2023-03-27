<script>
export default {
    name: "TheFooterBottom",
    data() {
        return {
            navLinks: [
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
        <div class="container">

        </div>
    </section>
</template>
  
<style lang="scss" scoped>
@use '../styles/partials/variables';

#footer-bottom {
    background-color: #303030;
    height: 25%;
    width: 100%;
}
</style>