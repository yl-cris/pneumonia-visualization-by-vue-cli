<template>
  <div class="main">
    <div class="left">
        <Left></Left>
    </div>
    
    <div class="right">
      <div class="top">
        <img src="img/title.jpg" alt />
      </div>
      <div class="bottom">
          <Right></Right>
      </div>
    </div>
  </div>
</template>
<style>
* {
  padding: 0;
  margin: 0;
}
.left{
    width:200px;
    float: left;
    margin-right: 10px;
}
.right{
    width:900px;
    float: right;
    margin-left: 10px;
}
.main{
    width: 1200px;
    margin: 20px auto;
}
.top img{
    height: 200px;
    width: 900px;
}
.left,.right{
    background-color: #cccaca;
    height: 700px;
}
</style>
<!--添加组件的引用和注册-->
<script>
import Left from '../components/Left.vue'
import Right from "../components/Right.vue";
export default {
    components:{
        Left,
        Right
    }
    
}
</script>