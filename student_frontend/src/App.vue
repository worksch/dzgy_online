<template>
  <div id="app">
    <!-- <router-view/> -->
    <!-- tabcontainer -->
    <mt-tab-container class="page-tabbar-container" v-model="selected">
      <mt-tab-container-item id="tab1">
        <div>焊接</div>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab2">
        <div>产口</div>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab3">
        <div>EDA</div>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab4">
        <div class="page-part">
        </div>
        <router-link to="/">
        <mt-button type="danger" size="large">退出</mt-button>
        </router-link>
      </mt-tab-container-item>
    </mt-tab-container>
    <mt-tabbar v-model="selected">
      <mt-tab-item id="tab1">
        <img slot="icon" src="./assets/logo.png">
        焊接
      </mt-tab-item>
      <mt-tab-item id="tab2">
        <img slot="icon" src="./assets/logo.png">
        产品
      </mt-tab-item>
      <mt-tab-item id="tab3">
        <img slot="icon" src="./assets/logo.png">
        EDA
      </mt-tab-item>
      <mt-tab-item id="tab4">
        <img slot="icon" src="./assets/logo.png">
        我
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
import btnMenu from './components/BottomMenu'

export default {
  name: 'App',
  components:{
    btnMenu
  },
  data() {
    return {
      selected: 'tab1'
    };
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
    overflow: hidden;
    height: 100vh;
}
  .page-wrap {
    overflow: auto;
    height: 100%;
    padding-bottom: 100px;
  }
</style>
