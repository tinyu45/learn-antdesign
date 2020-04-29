
<template>
    <a-carousel arrows autoplay>    
        <div class="item"><img src="@/assets/images/item-01.jpg"></div>
        <div class="item"> <img src="@/assets/images/item-02.jpg"></div>
        <div class="item"><img src="@/assets/images/item-03.jpg"></div>
        <div class="item"> <img src="@/assets/images/item-04.jpg"></div>
        <div class="item"><img src="@/assets/images/item-05.jpg"></div>
    </a-carousel>
</template>

<script>
export default {
components: {},
data() {
//这里存放数据
return {

};
},
//监听属性 类似于data概念
computed: {},
//监控data中的数据变化
watch: {},
//方法集合
methods: {

},
//生命周期 - 创建完成（可以访问当前this实例）
created() {

},
//生命周期 - 挂载完成（可以访问DOM元素）
mounted() {

},
beforeCreate() {}, //生命周期 - 创建之前
beforeMount() {}, //生命周期 - 挂载之前
beforeUpdate() {}, //生命周期 - 更新之前
updated() {}, //生命周期 - 更新之后
beforeDestroy() {}, //生命周期 - 销毁之前
destroyed() {}, //生命周期 - 销毁完成
activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
}
</script>
<style lang="scss" scoped>
    /* @import url(); 引入公共css类 */
   .ant-carousel{
        margin: 20px 0; 
        width: 100%;
        text-align: center;
        .item{
            width: 100%;
            img{
                margin: 0;
                padding: 0;
                width: 100%;
            }
        }
    }

    .ant-carousel >>> .slick-slide {
        text-align: center;
        height: 160px;
        line-height: 160px;
        background: #364d79;
        overflow: hidden;
    }

    .ant-carousel >>> .custom-slick-arrow {
        width: 25px;
        height: 25px;
        font-size: 25px;
        color: #000;
        background-color: rgba(31, 45, 61, 0.11);
        opacity: 0.3;
    }
    .ant-carousel >>> .custom-slick-arrow:before {
        display: none;
    }
    .ant-carousel  .custom-slick-arrow:hover {
        opacity: 0.5;
    }

    .ant-carousel >>> .slick-slide h3 {
        color: #fff;
    }

</style>