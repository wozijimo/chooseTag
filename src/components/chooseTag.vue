<template>
    
    <div class="cls-choostag">
        <div class="cls-item" v-for="(item,index) in getContent" :key="index" @click="clickTag(index)">
            <div v-bind:class="[clickIndex==index?`cls-titlestylebefore`:`cls-titlestyle`]">{{item.tagTitle}}</div>
            <div v-bind:class="[clickIndex==index?`cls-itemLinebefore`:`cls-itemLine`]" ></div>
        </div>
    </div>

</template>


<script>
export default {

    name:"ChooseTag",
    
    data(){
        return{
            clickIndex:"",
        }
    },

    props:{
        getContent:{
            style:Array,
            default:()=> {
                return[{
                    tagTitle:"选项卡1"
                },{
                    tagTitle:"选项卡2"
                },{
                    tagTitle:"选项卡3"
                }]
            }
        }
    },

    // watch:() => {
        
    // },

    methods:{
        clickTag(index){
            this.clickIndex = index;
            this.$emit("itemTagClick",index)
        }
    }

}
</script>

<style>
    .cls-choostag{
        display: flex;
        flex-flow: row;
        justify-content: space-around;
        align-items: center;
    }

    .cls-item{
        width: auto;
    }

    /* 点击之前字体颜色，默认黑色 */
    .cls-titlestyle{
        font-size: 14px;
        color: #000;
    }

    /* 点击之后，字体颜色变蓝 */
    .cls-titlestylebefore{
        font-size: 14px;
        color:#1E90FF;
    }

    /* 点击之前没有下滑线 */
    .cls-itemLine{
        height: 3px;
        background-color:#ffffff;
    }

    /* 点击之后是蓝色的下划线 */
    .cls-itemLinebefore{
        height: 3px;
        background-color:#1E90FF;
    }


</style>