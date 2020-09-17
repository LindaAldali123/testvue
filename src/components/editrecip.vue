<template>
 <div class="info2" @click.stop="product.klic"  v-if="product.klic" style="margin-left:700px; "  v-bind:key="product.id">
       URL : <input
            type="product"
            v-bind:value="product.img" style="width:480px; height:30px; margin-bottom:10px"
          /><br>
          <img v-bind:src="product.img" />
           <h2 style="margin-right:360px"> {{product.title}}</h2>
       <h4 style="margin-right:360px"> {{product.description}}</h4>
         <h6 class="col-md-6" style="margin-right:360px"> {{product.tit}} ({{product.nu1}})</h6>
          <h6 class="col-md-6" style="margin-right:360px"> {{product.tit2}} ({{product.nu2}})</h6>
        </div>   
</template>
<script>
import products from "./products";
export default {
    name:"editrecip",
    components:{
        products
    }
}
</script>
 