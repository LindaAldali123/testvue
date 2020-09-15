<template>
  <div class="row header">
    <ul>
      <router-link to="/recipes" tag="li" exact>
        <a>Recipes</a>
      </router-link>
      <router-link to="/about" tag="li">
        <a>Shoping List</a>
      </router-link>
      <router-link class="left" to="/login" tag="li" replace>
        <a>Logout</a>
      </router-link>
    </ul>
    <Dropdown class="drop" title="Manage" :items="Manage" />
  </div>
</template>
<script>
import Dropdown from "./Dropdown";
export default {
  name: "AppHeader",
  components: {
    Dropdown
  },
  data() {
    return {
      Manage: [
        {
          title: "Fetch Data",
          link: "#"
        },
        {
          title: "Save Data",
          link: "#"
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.header {
  background-color: rgb(230, 224, 224);
  overflow: hidden;
  border-radius: 5px;
  ul {
    float: left;
    width: calc(100%-200px);
    margin: 0;
    li {
      padding: 20px;
      display: inline-block;
      font-size: 18px;
      a {
        text-decoration: none;
      }
    }
  }
  .header ul .left {
    margin-left: 120px !important;
  }
}

.header .drop {
  margin-top: 20px !important;
}
</style>