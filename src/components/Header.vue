<template>
  <div id="Header">
    <h2>Vuest</h2>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped lang="scss">

  #Header {
    background: rgba(255, 255, 255, 0.6);
    position: absolute;
    width:100%;
    height: 50px;
    left: 0px;
    top: 0px;
    h2 {
      height: 22px;
      font-style: normal;
      font-weight: normal;
      font-size: 18px;
      line-height: 22px;
    }
  }
</style>
