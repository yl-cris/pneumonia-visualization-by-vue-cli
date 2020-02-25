<template>
    <div name="show">
        <ul class="goodlist">
            <li v-for="goods in list">
                <img v-bind:src="goods.img">
                <p>{{goods.goodName}}</p>
            </li>
        </ul>
    </div>
</template>
<style>
.goodlist li{
    width:200px;
    height:200px;
    list-style :none;
    float :left;
    font-size:9px;
    color:tomato;
    margin-left:30px;
    margin-bottom: 30px;

}
.goodlist img{
    width:850px;
    height: 450px;
}
</style>
<script>
export default {
    name:"show",
    data(){
        var obj=this;
        var url='';
        if (obj.goodId==1) {
            url="json/bjb.json";             
        }
        else if (obj.goodId==2) {
            url="json/sj.json";     
        }
        else if(obj.goodId==3){
            url="json/bar.json";
        }
        else if(obj.goodId==4){
            url="json/line.json";
        }
        else if(obj.goodId==5){
            url="json/pie.json";
        }
        else if(obj.goodId==6){
            url="json/geol.json";
        }
        else if(obj.goodId==7){
            url="json/hotel.json";
        }
        else if(obj.goodId==8){
            url="json/lei.json";
             }
        else{
            url="json/bjb.json"; 
        }
        this.$http.get(url).then(function(res){
            obj.list=res.data;

        })
        return{
            list:[]
        }
    },
    props:{
        goodId:Number
    },
    watch:{
        goodId(){
            var obj=this;
            var url='';
            if (obj.goodId==1) {
                url="json/bjb.json";             
            }
            else if (obj.goodId==2) {
                url="json/sj.json";     
            }
            else if(obj.goodId==3){
            url="json/bar.json";
            }
            else if(obj.goodId==4){
            url="json/line.json";
            }
            else if(obj.goodId==5){
            url="json/pie.json";
            }
            else if(obj.goodId==6){
            url="json/geol.json";
            }
            else if(obj.goodId==7){
            url="json/hotel.json";
             }
             else if(obj.goodId==8){
            url="json/lei.json";
             }
            else{
                url="json/bjb.json"; 
            }
            this.$http.get(url).then(function(res){
            obj.list=res.data;

        })
        return{
            list:[]
        }

        }
    }

}
</script>