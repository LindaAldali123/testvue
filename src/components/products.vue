<template>
  <div class="products">
    <button
      class="row col-md-6"
      v-for="product in products"
      v-bind:key="product.id"
      @click.prevent="product.klic = !product.klic"
    >
      <div class="col-md-3">
        <h2>{{product.title}}</h2>
        <h6>{{product.description}}</h6>
      </div>
      <div class="img col-md-2">
        <img v-bind:src="product.img" />
        <!--<img src="../assets/meat.jpg" >-->
      </div>
      <transition class="trans" name="fade"  appear>
        <div class="info" @click.stop="product.klic"  v-if="product.klic" style="margin-left:700px; "  v-bind:key="product.id">
         <!--URL : <input
            type="product"
            v-bind:value="product.img" style="width:480px; height:30px; margin-bottom:10px"
          /><br>-->
          <img v-bind:src="product.img" />
           <h2 style="margin-right:360px"> {{product.title}}</h2>
       <Dropdown2  style="margin-right:330px; border-radius:5px; width:180px; background-color:green; color:#FFF !important; padding:15px" class="drop" title="Manage Recipe" :items="Manage"/>
        <h4 style="margin-right:360px"> {{product.description}}</h4>
         <h6 class="col-md-6" style="margin-right:360px"> {{product.tit}} ({{product.nu1}})</h6>
          <h6 class="col-md-6" style="margin-right:360px"> {{product.tit2}} ({{product.nu2}})</h6>
        </div>
      </transition>
    </button>
  </div>
</template>

<script>
import Dropdown2 from "./Dropdown2";
export default {
  name: "products",
   components: {
    Dropdown2
  },
  data: function() {
    return {
      products: [
        {
          id: 1,
          title: "cake",
          description: "Syrian cake",
          img: require("../assets/cake.jpg"),
          tit:"sugher ",
          tit2:"eggs",
          nu1:2,
          nu2:3,
         klic: false
        },
        {
          id: 2,
          title: "meat",
          description: "Syrian meat",
          img: require("../assets/meat.jpg"),
           tit:"proteen ",
          tit2:"chiken",
          nu1:2,
          nu2:3,
          klic: false
        },
        {
          id: 3,
          title: "pizaa",
          description: "Syrian pizaa",
          img: require("../assets/pizaa.jpg"),
           tit:"tomato ",
          tit2:"salt",
          nu1:2,
          nu2:1,
          klic: false
        },
        {
          id: 4,
          title: "vegitable",
          description: "Syrian vegitable",
          img: require("../assets/vege.jpg"),
           tit:"appel",
          tit2:"bananas",
          nu1:4,
          nu2:3,
          klic: false
        },
        {
          id: 5,
          title: "cake",
          description: "Syrian cake",
          img: require("../assets/cake.jpg"),
           tit:"sugher",
          tit2:"eggs",
          nu1:2,
          nu2:3,
          klic: false
        },
        {
          id: 6,
          title: "meat",
          description: "Syrian meat",
          img: require("../assets/meat.jpg"),
           tit:"proteen ",
          tit2:"chiken",
          nu1:2,
          nu2:3,
          klic: false
        },
        {
          id: 7,
          title: "pizaa",
          description: "Syrian pizaa",
          img: require("../assets/pizaa.jpg"),
           tit:"tomato ",
          tit2:"salt",
          nu1:2,
          nu2:3,
          klic: false
        },
        {
          id: 8,
          title: "vegitable",
          description: "Syrian vegitable",
          img: require("../assets/vege.jpg"),
          tit:"appel",
          tit2:"bananas",
          nu1:2,
          nu2:3,
          klic: false
        }
      ],
      Manage: [
        {
          title: "To Shopping List",
          link: "/about"
        },
        {
          title: "Edit Recipe",
          link: "#"
        },
        {
          title: "Delete Recipe",
          link: "#"
        }
      ]
      
    };
  }
};
</script>
<style scoped>
.col-md-6 {
  margin-left: 36px !important;
  margin: 0;
  padding: 0;
  border: 1px solid rgb(245, 235, 235);
  background-color: #fff;
}
.img img {
  float: left;
  width: 90px !important;
  height: 70px;
  margin-top: 10px;
  margin-left: 180px;
}
button:hover {
  background-color: rgb(85, 189, 166);
}
/*
.products .row .trans {
  margin-left: 200px !important;
  transform: translateX(600px);
  border: 1px solid #ddd;
  width: 50px;
  height: 60px;
}*/
.products .col-md-6 .trans .info img {
  border: 2px solid rgb(77, 75, 75);
  width: 50px !important;
  height: 60px;
}
.info h6{
    padding:12px;
    border:1px solid #DDD;
    margin-right: 90px;
}
</style>