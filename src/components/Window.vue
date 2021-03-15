<template>
  <div class="WindowCl" v-if="data">
    <form action="#">
      <input v-model="title" class="Title" type="search" placeholder="Title...">
      <textarea v-model="text" name="text" id="inputText" placeholder="Lorem ninja ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut ninja wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit ninja lobortis nisl ut aliquip ex ea commodo consequat. Duis ninja autem vel eum iriure dolor in hendrerit in vulputate ninja velit esse molestie consequat, vel illum dolore eu feugiat nulla ninja facilisis at vero eros et accumsan et iusto odio..."></textarea>
      <button type="button" class="btn" @click="WindowClose">Add a new Blog </button>
    </form>
  </div>
</template>

<script>


export default {
  name: 'Window',
  data() {
    return{    
    }
  },
  props: ['data'],
  methods: { 
    WindowClose() {
      this.$emit('update', [
        {IsFalse: false},
        this.title,
        this.text
      ])
      document.querySelector('#Header').style.opacity = '1'
      document.querySelector('.blog').style.opacity = '1'
    }
  }
}
</script>

<style scoped lang="scss">

  .WindowCl {
    display: block;
    z-index: 100;
    position: absolute;
    top: 65px;
    left: 38%;
    width: 385px;
    height: 580px;
    background: linear-gradient(249.73deg, #61FFEC 0%, #AA76FF 100%);
    border-radius: 5px;
    padding-left: 2%;
    padding-right: 2%;
    .Title {
      position: relative;
      top: 30px;
      border: none;
      padding: 10px;
      width: 350px;
      height: 46px;
      background: rgba(34, 34, 34, 0.6);      
      font-size: 16px;
    }
    #inputText {
      padding: 10px;
      font-size: 16px;
      position: relative;
      top: 60px;
      left: -10px;
      resize: none;
      width: 100%;
      height:350px;
      background: rgba(34, 34, 34, 0.6);
    }
    .btn {
      position: absolute;
      bottom: 40px;
      left: 25%;
       width: 220px;
      height: 40px;
      background: rgba(72, 255, 167, 0.8);
      border-radius: 10px;
      border: none;
      color: white;
      // Текст
      font-style: normal;
      font-weight: 500;
      font-size: 18px;
      line-height: 22px;
    }
  }
</style>
