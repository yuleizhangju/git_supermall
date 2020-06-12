<template>

  <div class="nav-bar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>

  </div>
</template>

<script>
    export default {
        name: "NavBar"
    }
</script>

<style scoped>
.nav-bar{

  display:flex;
  line-height:44px;
  height:44px;
  background-color:#2A5C86;
  color: #ffffff;
}

  .left, .right{

   width:60px;
    text-align: center;
  }

  .center{

    flex:1;
    text-align: center;
  }


</style>