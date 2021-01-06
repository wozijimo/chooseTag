<template>
    
    <div>

        <VChatTitle v-bind:titleContent="chat2Obj"></VChatTitle>

    </div>

</template>


<script>

import VChatTitle from '../components/VChatTitle.vue'
import circleAdd from '../assets/circleAdd.png'

export default {

    components:{
        VChatTitle,
        circleAdd
    },

    data(){
        return{
            chat2Obj:{
                title:"微信首页",
                right:circleAdd,
            },
        }
    }



}
</script>

<style>
    


</style>