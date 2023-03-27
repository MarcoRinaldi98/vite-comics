<template>
  <header>
    <TheHeader />
  </header>

  <main>
    <div class="container">
      <h2> Content goes here </h2>
    </div>
  </main>

  <footer>
    <TheFooterTop />
    <TheFooterCenter />
    <TheFooterBottom />
  </footer>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheFooterTop from './components/TheFooterTop.vue';
import TheFooterCenter from './components/TheFooterCenter.vue';
import TheFooterBottom from './components/TheFooterBottom.vue';

export default {

  components: {
    TheHeader,
    TheFooterTop,
    TheFooterCenter,
    TheFooterBottom
  }

}
</script>

<style lang="scss">
@use "./styles/general.scss";
</style>
