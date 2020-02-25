<template>
    <div>
        <div v-if="kk==1">
           <Goodlist goodId="1"></Goodlist>
        </div>
        <div v-else-if="kk==2">
           <Goodlist goodId="2"></Goodlist>
        </div>
        <div v-else-if="kk==3">
            <Goodlist goodId="3"></Goodlist>
        </div>
        <div v-else-if="kk==4">
            <Goodlist goodId="4"></Goodlist>
        </div>
        <div v-else-if="kk==5">
            <Goodlist goodId="5"></Goodlist>
        </div>
        <div v-else-if="kk==6">
            <Goodlist goodId="6"></Goodlist>
        </div>
        <div v-else-if="kk==7">
            <Goodlist goodId="7"></Goodlist>
        </div>
        <div v-else-if="kk==8">
            <Goodlist goodId="8"></Goodlist>
        </div>
        <div v-else>
            <Goodlist goodId="0"></Goodlist>
        </div>
    </div>
</template>
<script>
import Msg from "../components/msg.js";
import Goodlist from '../components/goodlist.vue'
export default {
    data(){
        return{
            kk:0
        }
    },
    mounted:function(){
        var _this=this;
        Msg.$on('val',function(m){
            _this.kk=m;
        })
    },
    components:{
        Goodlist

    }
    
}
</script>