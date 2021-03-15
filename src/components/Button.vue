<template>
  <div id="btn">
    <button @click="buttonClick"> Add a new Blog</button> 
    <Window :data='isTrue' @update='updateFun'/>
    <div class="blog">
      <Comment 
      v-for="List in Lists"
      :key="List.title"
      :List="List"
      />
    </div>
  </div>
</template>

 
<script>

import Comment from './Comment'
import Window from './Window'

export default {
  components: { Window, Comment },
  name: 'Button',
  data() {
    return {
      isTrue: false,
      title:'',
      text:'',
      Lists: []
    }
  },
  methods: {
    buttonClick() {
      this.isTrue = true
      document.querySelector('#Header').style.opacity = '.2'
      document.querySelector('.blog').style.opacity = '.2'
    },
    updateFun(param) {
      this.Lists.push({title:param[1], text:param[2]})
      this.isTrue = param.IsFalse
    },
  }
}
</script>


<style scoped lang="scss">
  #btn{
    margin-top: 10px;
    button {
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
