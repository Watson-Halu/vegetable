<template>
  <!-- <v-main padding="0"> -->
    <!-- Provides the application the proper gutter -->
    <v-container fluid pa-0>
      <div class="topView">
        <div class="topText">
          <img src="../assets/topLabel.png" fluid/>
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
<style lang="scss" scoped>
  /* .topView_container{
    padding: 0
  } */
  .topView{
    height: 100vh;
    background-image: url("../assets/topBG.jpg");
    background-size: cover;
    background-repeat: no-repeat center;
    padding: 0;
    margin: 0;
  }
  .topText{
    position: relative;
    opacity: 0.8;
    width: 100%;
    img{
      transform: scale(0.6);
      width: 100%;
      position: relative;
      top: -20vh;
      transform: scale(0.35)
    }
    p{
      text-align: center;
    }
  }
  @media screen and (max-width:1024px){
    .topText{
      img{
        top: 25vh;
      transform: scale(1.2)
      }
    }
  }

</style>
