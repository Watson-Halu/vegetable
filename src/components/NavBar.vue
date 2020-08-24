<template>
  <v-app-bar app>
    <ul class="nav-list-left">
      <li class="nav-item">
        <span>
          <img src="../assets/vegetable_name.png">
        </span>
      </li>
    </ul>
    <ul class="nav-list-right">
      <li class="nav-item">
        <span>About Us 食堂起源</span>
      </li>
      <li class="nav-item">
        <span>Mune 素說菜單</span>
      </li>
      <li class="nav-item">
        <span>Contact Us 找到食堂</span>
      </li>
    </ul>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavBar',
  data: () => ({

  })
}
</script>
<style scoped>
  .nav-list-left{
    list-style: none;
  }
  .nav-list-left img{
    width: 38%;
    position: relative;
    top: 4px;
  }
  .nav-list-right{
    display: flex;
    justify-content: flex-end;
    width: 100%;
    list-style: none;
    cursor: pointer;
  }
  .nav-item{
    margin-right: 18px;
  }
</style>
