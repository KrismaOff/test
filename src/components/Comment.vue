<template>
    <div class="comment">
        <div class="title">
          <ul>
            <li>{{ List.title }}</li>
          </ul>
        </div>
        <div class="mainText">
           <ul>
             <li>{{ List.text }}</li>
          </ul>
        </div>
        <div class="author">
          <img src="../assets/user.svg" alt="Icon"> 
          <span>Krisma OFF</span>
        </div>
        <button class="show">Show more</button>
    </div>
</template>

<script>
export default {
  name: 'Comment',
  props: ['List']
}
</script>
<style scoped lang="scss">

    %ul {
      ul {
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 19px;
        list-style-type: none;
        li {
          display: inline-block;
          margin-right: 5px;
        }
      }
    }

    .all {
    display: block;
  }
  .comment{
    position: relative;
    width: 600px;
    height: 180px;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 10px;
    padding: 20px;
    text-align: left;
    margin: 20px;
    .title {
      position: absolute;
      top: 0px;
      left: -20px;
      @extend %ul
    }
    .mainText {
      font-style: normal;
      font-weight: normal;
      font-size: 10px;
      line-height: 18px;
      position: absolute;
      top: 35px;
      left: -20px;
      width: 95%;
      ul {
        font-size: 13px;
      }
      @extend %ul
    }
    .author {
      font-style: normal;
      font-weight: normal;
      font-size: 10px;
      line-height: 12px;
      position: absolute;
      bottom: 20px;
      display: flex;
      img {
        height: 20px;
        position: relative;
        bottom: 5px;
        right: 5px;
      }
      span {
        font-style: normal;
        font-weight: normal;
        font-size: 12px;
        line-height: 12px;
      }
    }
    .show {
      background: #AA76FF;
      border-radius: 10px;
      border: none;
      position: absolute;
      bottom: 20px;
      right: 20px ;
      padding: 5px;
      transition: .5s;
      &:hover {
        color: white;
        background: #8f5ce0;
      }
    }
  }

</style>
