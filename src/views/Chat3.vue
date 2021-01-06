<template>
    
    <VChatTitle v-bind:titleContent="chat3Obj">

        <ChooseTag v-bind:getContent="chooseTagArr" slot="chooseTag"></ChooseTag>

    </VChatTitle>

</template>

<script>
import VChatTitle from '../components/VChatTitle.vue'
import backImg from '../assets/back.png'
import settingImg from '../assets/setting.png'
import ChooseTag from '../components/chooseTag.vue'

export default {

  components: {
      VChatTitle,
      backImg,
      settingImg,
      ChooseTag
      },

   
    data(){
        return{
             chat3Obj:{
                left:backImg,
                right:settingImg,
            },

            chooseTagArr:[{
                    tagTitle:"精选表情"
                },{
                    tagTitle:"更多表情"
                }]
        }
    },

}
</script>


<style>



    
</style>