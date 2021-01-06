<template>
  <div>
      <ChooseTag v-bind:getContent="tagArr" v-on:itemTagClick="itemTagClick"></ChooseTag>
      <div class="cls-show">{{showText}}</div>
    
  </div>
</template>

<script>

import ChooseTag from "@/components/chooseTag.vue"


export default {

  components:{
    ChooseTag
  },

  data(){
    return{
      i:"",
      showText:"选项卡1被点击",
      tagArr:[
        {
          tagTitle:"选项卡1"
        },{
          tagTitle:"选项卡2"
        },{
          tagTitle:"选项卡3"
        },{
          tagTitle:"选项卡4"
        }
      ]
    }
  },

  methods:{

    itemTagClick(index){
      console.log(this.tagArr[0].tagTitle);
        this.showText = this.tagArr[index].tagTitle +"被点击"
    }
  }

  
}
</script>

<style>
  
  .cls-show{
    width: max;
    height: 500px;
    background-color: #eeeeee;
  }

</style>