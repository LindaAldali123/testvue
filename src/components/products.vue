<template>
    <div class="products ">
        <button class="row col-md-6" v-for="product in products" v-bind:key="product.id">
   <div class="col-md-3">
     <h2>{{product.title}}</h2>
      <h6>{{product.description}}</h6>
     </div>
    <div class="img col-md-2"  >
  <img  v-bind:src="product.img">
  <!--<img src="../assets/meat.jpg" >-->
   </div>
</button>
    </div>
</template>

<script>
export default {
  name:"products" ,
   data:function(){
       return{
      products:[
          {
id:1,              
title:"cake",
description:"Syrian cake",
img: require('../assets/cake.jpg')
          },{
id:2,
title:"meat",
description:"Syrian meat",
img:require("../assets/meat.jpg")
          },{
id:3,              
title:"pizaa",
description:"Syrian pizaa",
img:require("../assets/pizaa.jpg")
          }
          ,{
id:4,              
title:"vegitable",
description:"Syrian vegitable",
img:require("../assets/vege.jpg")
          },
          {
id:5,              
title:"cake",
description:"Syrian cake",
img:require( "../assets/cake.jpg")
          },{
id:6,
title:"meat",
description:"Syrian meat",
img:require("../assets/meat.jpg")
          },{
id:7,              
title:"pizaa",
description:"Syrian pizaa",
img:require("../assets/pizaa.jpg" )
          }
          ,{
id:8,              
title:"vegitable",
description:"Syrian vegitable",
img:require("../assets/vege.jpg" )
          }
      ]
       };
   }
};
</script>
<style scoped>
.col-md-6{
    margin-left: 36px !important;
    margin:0;
    padding:0;
    border: 1px solid  rgb(245, 235, 235);
    background-color:#FFF;

}
.img img {
    float: left;
    width: 90px !important;
    height: 70px;
    margin-top: 10px;
    margin-left: 180px;
}
button:hover{
    background-color: rgb(85, 189, 166);
    
}

</style>