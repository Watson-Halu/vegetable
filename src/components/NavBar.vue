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
          <span class="subtext">{{ item.subtext }}</span>
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
        { name: '素說菜單', subtext: 'Menu', id: 'menu' },
        { name: '食堂起源', subtext: 'About Us ', id: 'begin' },
        { name: '找到食堂', subtext: 'Contact Us ', id: 'location' }
      ]
    }
  },
  methods: {
    goto (refName) {
      var element = document.getelementById(refName)
      console.log(element)
      var top = element.offsetTop
      window.scrollTo(0, top)
    }
  }
}
</script>
<style lang="scss" scoped>
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
    text-align: center;
    .subtext{
      display: block;
    }
  }
  @media only screen and (max-width:1024px){
    .nav-list-left{
      padding-left:0;
      width: 80%;
      img{
        width: 80%;
      }
    }
    .nav-list-right{
      width: 120%;
      font-size:.9rem;
      padding-left: 0mm;
      // display: flex;
      // justify-items: ;;
    }
  }
  @media only screen and (max-width:767px){
    .nav-list-left{
      img{
        transform: scale(1.75)
      }
      .nav-item{
        text-align: left;
      }
    }
    .nav-list-right{
      .nav-item{
        font-size: .7rem;
        margin-right: 8px;
      }
    }
    .nav-item{
      margin-right:0;
    }
  }
</style>
