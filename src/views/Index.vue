<template>
 <a-layout id="components-layout-demo-fixed">
    <a-layout-header :style="{ position: 'fixed', zIndex: 1, width: '100%' }">
      <div class="logo">
        <img src="@/assets/images/logo.jpg">
      </div>
      <a-menu
        theme="dark"
        mode="horizontal"
        :defaultSelectedKeys="['/']"
        :style="{ lineHeight: '64px' }"
        @click="clickHandler"
      >
        <a-menu-item key="/">首页</a-menu-item>
        <a-menu-item key="product" >产品</a-menu-item>
        <a-menu-item key="dynamic" >动态</a-menu-item>
        <a-menu-item key="contact" >联系</a-menu-item>
      </a-menu>
    </a-layout-header>
    <!-- <a-layout-content :style="{ padding: '0 50px', marginTop: '64px' }"> -->
    <a-layout-content :style="{ marginTop: '64px' }">
      <router-view/>
      <!-- <a-breadcrumb :style="{ margin: '16px 0' }">
        <a-breadcrumb-item>Home</a-breadcrumb-item>
        <a-breadcrumb-item>List</a-breadcrumb-item>
        <a-breadcrumb-item>App</a-breadcrumb-item>
      </a-breadcrumb>
      <div :style="{ background: '#fff', padding: '24px', minHeight: '380px' }">Content</div> -->
    </a-layout-content>
    <a-layout-footer :style="{ textAlign: 'center' }">
      Ant Design ©2018 Created by Ant UED
    </a-layout-footer>
  </a-layout>
</template>

<script>
export default {
  name: 'Index',
  data(){
    return {

    }
  },

  methods:{
    // selectHandler(e){
    //   console.log('select', e)
    // },

    clickHandler(e){
      console.log('click', e.key)
      this.$router.push(e.key);
    }
  }


}
</script>

<style lang="scss" scoped>
    .logo {
          width: 120px;
          height: 64px;
          line-height: 64px;
          //background: rgba(255, 255, 255, 0.2);
          float: left;
          // text-align: center;
          img{
            width: 60px;
            height: 60px;
            vertical-align: middle;
            border-radius: 30px;
            overflow: hidden;
            border: 2px solid #666;
          }
      }
</style>
