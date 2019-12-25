<template>
  <div id="app">
    <HeaderBar />
    <div class="main-section content-title-group">
      <div style="height: 50px;">
      <!-- <Slider /> -->
      </div>
      <!-- <h2 class="title">Heroes</h2>
      <div>We'll start here</div> -->
      <ComingSoon />
      <Contact />
    </div>
  </div>
</template>

<script>
import HeaderBar from '@/components/header-bar';
import Slider from '@/components/slider';
import ComingSoon from '@/components/coming-soon';
import Contact from '@/components/contactform';

export default {
  name: 'App',
  components: { HeaderBar, Slider, ComingSoon, Contact },
};
</script>

<style lang="scss">
@import '@/design/index.scss';
</style>
