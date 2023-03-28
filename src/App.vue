<template>
  <header>
    <TheHeader :nav="navLinks" />
  </header>

  <main>
    <TheHero />
    <TheMain />
  </main>

  <footer>
    <TheFooterTop :image="imageList" />
    <TheFooterCenter :fLinks="footerLinks" />
    <TheFooterBottom :icon="iconList" />
  </footer>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheHero from './components/TheHero.vue';
import TheMain from './components/TheMain.vue';
import TheFooterTop from './components/TheFooterTop.vue';
import TheFooterCenter from './components/TheFooterCenter.vue';
import TheFooterBottom from './components/TheFooterBottom.vue';

export default {

  components: {
    TheHeader,
    TheHero,
    TheMain,
    TheFooterTop,
    TheFooterCenter,
    TheFooterBottom
  },
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
      ],
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
      ],
      footerLinks: [
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
      ],
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

<style lang="scss">
@use "./styles/general.scss";
</style>
