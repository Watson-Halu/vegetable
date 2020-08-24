<template>
  <!-- <v-main padding="0"> -->
    <!-- Provides the application the proper gutter -->
    <v-container fluid class="topView_container">
      <div class="topView">
        <div class="topText">
          <img src="../assets/Styling_Vegetable_2.png" fluid/>
        </div>
      </div>
      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  <!-- </v-main> -->

  <!--<v-footer app>
  </v-footer>-->
</template>

<script>
export default {
  name: 'TopContent',

  data: () => ({

  })
}
</script>
<style scoped>
  .topView_container{
    padding: 0
  }
  .topView{
    height: 100vh;
    background-image: url("../assets/topView_bg.jpg");
    background-size: cover;
    background-repeat: no-repeat center;
    padding: 0;
    margin: 0;
  }
  .topText{
    position: relative;
    opacity: 0.8;
    width: 100%;
  }
  .topText img{
    transform: scale(0.85);
    width: 100%;
    position: relative;
    top: 10vh;
  }

</style>
