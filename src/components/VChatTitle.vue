<template>
    
    <div class="cls-itemAll">

        <!-- 返回图标及未读消息 -->
        <div class="cls-itemLeft">
            <img class="cls-itemLeftImg" v-bind:src="titleContent.left" alt="">
            <slot name="cls-itemLeftNumber"></slot>
            <!-- <div class="cls-itemLeftNumber">1</div> -->
        </div>

        <!-- 标题 -->
        <!-- 群名字及成员数量 -->
        <div class="cls-itemCenter">
            <div class="cls-itemCenterName">{{titleContent.title}}</div>
            <slot name="cls-itemCenterName"></slot>
            <!-- <div class="cls-itemCenterNumber">(1)</div> -->
        </div>

        <!-- 选项卡 -->
        <slot name="chooseTag"></slot>

        <!-- 更多设置 -->
        <img class="cls-itemRight" v-bind:src="titleContent.right" alt="">


    </div>
</template>

<script>

import leftImg from '../assets/back.png'
import rightImg from '../assets/more.png'

export default {

    components:{
        leftImg,
        rightImg
    },

    props:{
        titleContent:{
            type:Object,
            default:()=>{
                return{
                title:"默认名称",
                left:leftImg,
                weidushu:"",
                qunyuanshu:"",
                right:rightImg,
                }
            },
        }
    }




}
</script>

<style>
    
    .cls-itemAll{
        height: 65px;
        width: 400px;
        display: flex;
        flex-flow: row;
        justify-content: space-between;
        align-items: center;
        background-color: #efefef;
    }

    .cls-itemLeft{
        display: flex;
        flex-flow: row;
        justify-content: center;
        align-items: center;
        margin-left: 20px;
    }

    .cls-itemLeftImg{
        height: 30px;
    }

    .cls-itemLeftNumber{
        width: 30px;
        height: 30px;
        line-height:30px;
        text-align: center;
        background-color: #cccccc;
        border-radius: 15px;
    }

    .cls-itemCenter{
        display: flex;
        flex-flow: row;
        justify-content: center;
        align-items: center;
    }


    

    .cls-itemRight{
        height: 25px;
        margin-right: 20px;
    }
</style>