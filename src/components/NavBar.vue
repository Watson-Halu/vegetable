<template>
  <v-app-bar app>
    <ul class="nav-list-left">
      <li class="nav-item">
        <span>
          <img src="../assets/logoName_.png">
        </span>
      </li>
    </ul>
    <ul class="nav-list-right">
      <li class="nav-item"  v-for="item of items" :key="item.name" @click="scrollTo(item.id)">
        <span>
          {{ item.name }}
        </span>
      </li>
    </ul>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavBar',
  data () {
    return {
      items: [
        { name: 'Menu 素說菜單', id: 'menu' },
        { name: 'About Us 食堂起源', id: 'begin' },
        { name: 'Contact Us 找到食堂', id: 'location' }
      ]
    }
  },
  methods: {
    goto (refName) {
      var element = this.$refs[refName]
      console.log(element)
      var top = element.offsetTop
      window.scrollTo(0, top)
    }
  }
}
</script>
<style scoped>
  .nav-list-left{
    list-style: none;
  }
  .nav-list-left img{
    width: 70%;
    position: relative;
    top: 8px;
  }
  .nav-list-right{
    display: flex;
    justify-content: flex-end;
    width: 100%;
    list-style: none;
    cursor: pointer;
  }
  .nav-item{
    margin-right: 50px;
  }
</style>
