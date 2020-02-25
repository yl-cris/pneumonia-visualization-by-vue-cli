<template>
  <div>
    <div class="title">菜单</div>
    <ul class="menu">
      <li @click="menu1">新冠肺炎预防措施</li>
      <li @click="menu2">疫情地图渲染</li>
      <li @click="menu3">疫情直方图</li>
      <li @click="menu4">疫情折线图</li>
      <li @click="menu5">疫情饼图</li>
      <li @click="menu6">疫区人口迁徙情况</li>
      <li @click="menu7">轻症患者收治点情况</li>
      <li @click="menu8">重症患者收治点情况</li>
    </ul>
  </div>
</template>
<style scoped>
.title{
    width:200px;
    color: red;
    height: 30px;
    line-height: 30px;
    text-align: center;
}
.menu li{
    list-style: none;
    height: 50px;
    margin-bottom: 20px;
    background-color: white;
    line-height: 50px;
    cursor: pointer;
    margin-left:10px;
    margin-right: 10px;
}

</style>
<script>
import Msg from '../components/msg.js'
export default {
    methods:{
        menu1:function(){
            Msg.$emit("val","1");
        },
        menu2:function(){
            Msg.$emit("val","2");
        },
        menu3:function(){
            Msg.$emit("val","3");
        },
        menu4:function(){
            Msg.$emit("val","4");
        },
        menu5:function(){
            Msg.$emit("val","5");
        },
        menu6:function(){
            Msg.$emit("val","6");
        },
        menu7:function(){
            Msg.$emit("val","7");
        },
        menu8:function(){
            Msg.$emit("val","8");
        }
        
    }
}
</script>