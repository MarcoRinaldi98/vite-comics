<script>
export default {
    name: "TheFooterCenter",
    data() {
        return {
            navLinks: [
                {
                    name: 'dc comics',
                    type: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    name: 'shop',
                    type: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                },
                {
                    name: 'DC',
                    type: [
                        'Term of Use',
                        'Privacy policy (new)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    name: 'sites',
                    type: [
                        'DC',
                        'MAD Magazine',
                        'DC kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                }
            ]
        }
    }
}
</script>

<template>
    <section id="footer-center">
        <div class="container">

        </div>
    </section>
</template>
   
<style lang="scss" scoped>
@use '../styles/partials/variables';

#footer-center {
    background-image: url(../assets/footer-bg.jpg);
    height: 50%;
    width: 100%;
}
</style>