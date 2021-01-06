<template>
    
    <div>
        
        <VChatTitle  v-bind:titleContent="titleObj">

            <div slot="cls-itemLeftNumber" class="cls-itemLeftNumber">{{titleObj.weidushu}}</div>
            <div slot="cls-itemCenterName" class="cls-itemCenterNumber">({{titleObj.qunyuanshu}})</div>

        </VChatTitle>
        
    </div>
</template>

<script>
import VChatTitle from '../components/VChatTitle.vue'
import leftImg from '../assets/back.png'
import rightImg from '../assets/more.png'

export default {

  components: {

      VChatTitle,
      leftImg,
      rightImg

    },

    data(){
        return{
            titleObj:{
                title:"我是标题名称",
                left:leftImg,
                weidushu:"2",
                qunyuanshu:"11",
                right:rightImg,
            },
        }
    }
    
}
</script>


<style>
    
    

</style>