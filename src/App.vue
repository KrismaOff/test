<template>
<div>
  <Header/>
  <Button/>
</div>
</template>

<script>
import Header from './components/Header'
import Button from './components/Button'
export default {
  name: 'App',
  components: { Header, Button },
  data(){
    return{ 
    }
  },
}
</script>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  justify-content: center;
}
</style>
