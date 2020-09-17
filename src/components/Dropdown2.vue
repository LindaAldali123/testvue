<template>
  <div class="menu-item" @click="isOpen = !isOpen">
    <a href="#">{{title}}</a>
    <img src="../assets/arrow.png" />
    <transition name="fade" appear>
      <div class="sub-menu" v-if="isOpen">
        <div v-for="(item,i) in items" :key="i" class="menu-item">
          <a :href="item.link">{{item.title}}</a>
        </div>
      </div>
    </transition>
  </div>
</template>
<script>
//import Manage from "./AppHeader";
export default {
  name: "Dropdown2",
 props: ["title", "items"],
  data() {
    return {
      isOpen: false
    };
  }
};
</script>

<style>
nav .menu-item .sub-menu {
  position: absolute;
  top: calc(100% + 18px);
  background-color: rgb(60, 116, 4);
  left: 50%;
  transform: translateX(-50%);
  width: max-content;
  border-radius: 0px 0px 16px 16px;
}
.fade-enter-active,
.fade-leave-active {
  transition: all 0.5s ease-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>