<template>
  <div id="app">
    <HeaderBar />
    <div class="main-section content-title-group">
      <div style="height: 420px;">
      <Slider />
      </div>
      <h2 class="title">Heroes</h2>
      <div>We'll start here</div>
    </div>
  </div>
</template>

<script>
import HeaderBar from '@/components/header-bar';
import Slider from '@/components/slider'

export default {
  name: 'App',
  components: { HeaderBar, Slider },
};
</script>

<style lang="scss">
@import '@/design/index.scss';
</style>
