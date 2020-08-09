<template>
  <div class="bottom">
    <div class="item" @click="clickItem('/basic')" :class="{active: $route.path==='/'}">
      <i class="iconfont icon-shouye1"></i>
      <p>考核</p>
    </div>
    <div class="item" @click="clickItem('/product')" :class="{active: $route.path==='/'}">
      <i class="iconfont icon-shouye1"></i>
      <p>产口</p>
    </div>
    <div class="item" @click="clickItem('/creative')" :class="{active: $route.path==='/'}">
      <i class="iconfont icon-shouye1"></i>
      <p>创意</p>
    </div>
    <div class="item" @click="clickItem('/my')" :class="{active: $route.path==='/myhome'}">
      <i class="iconfont icon-wode"></i>
      <p>我的</p>
    </div>
  </div>
</template>
 
<script>
    export default {
      name: "bottom",
      methods:{
        clickItem:function(path){
            this.$router.push(path);
        }
      }
 
    }
</script>
 
<style scoped>
  /*@import "./../icon/iconfont.css";*/
  .bottom{
    position: fixed;
    bottom:0px;
    border-top:1px solid #d2d2d2;
    background-color: #f2f2f2;
    width: 100%;
    height:60px;
  }
  .item{
    margin:5px 20%;
    float:left;
  }
  .item p{
    margin:0;
    font-size: 15px;
  }
  .active{
    color:#108b70;
  }
</style>