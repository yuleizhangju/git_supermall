<template>
  <div id="app" class="wrap">
    <router-view></router-view>
    <main-tab-bar></main-tab-bar>
    <h1>你好！</h1>
  </div>
</template>

<script>
  import MainTabBar from 'components/content/mainTabbar/MainTabBar';

export default {
  name: 'App',
  components: {
    MainTabBar,
  }
}
</script>

<style>
@import 'assets/css/base.css';

</style>
