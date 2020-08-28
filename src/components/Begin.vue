<template>
  <!-- <v-main padding="0"> -->
    <!-- Provides the application the proper gutter -->
    <v-container fluid pa-0>
      <div class="connectAreaLeft">
      </div>
      <div class="connectAreaRight">
      </div>
      <div class="bottomView"  id="begin">
        <div class="begin">
          <h1>
            <span class="mainTitle">食堂起源</span>
          </h1>
          <span class="subTitle">
            About Us
          </span>
          <div class="mainContent">
            <div class="content">
              「素說食堂」為新式素食餐廳。<br>
              主廚有著十多餘年的素食餐點烹調經驗。<br>
              有感於大台中區素食人口逐漸上升，然素食餐點的變化卻難有突破。<br>
              <br>
              為了提供更多樣化的素食餐點，遂打造「素說食堂」素食品牌<br>
              <br>
                現階段因應饕客習慣，尚保留素食自助餐供應。<br>
                但同時提供了一人份量的素食套餐。
              <br>在未來，我們致力於改變一般素食的印象，不斷的開發新式素食餐點。
              <br>
              <br><span>希冀每次都能用不一樣的餐點內容，迎接每一次上門的你。</span>
            </div>
          </div>
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
  name: 'Begin',

  data: () => ({

  }),
  methods: {
  }
}
</script>
<style lang="scss" scoped>
  $color_word: #faecb9;
  $color_main: #729ea1;
  .bottomView{
    height:100vh;
    background-image: url(../assets/bottomBG.jpg);
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center center;
    padding-top: 20vh;
    margin-bottom: 10vh;
    .begin{
      text-align: center;
      background-color: rgba(255,255,255,0.7);
      padding: 50px;
      margin: 2vh 10% 5vh 10%;
      .mainTitle{
        border-bottom: 2px solid #000;
      }
      .subTitle{
        display: block;
        color: #000;
      }
      .mainContent{
        margin-top: 5vh;
      }
      .information{
        text-align: center;
      }
    }
  }
  @media only screen and (max-width:1024px){
    .bottomView{
      height: 80vh;
      padding-top: 20vh;
      background-size: cover;
    }
  }
  @media only screen and (max-width:768px){
    .bottomView{
      height: 120vh;
      padding-top: 10vh;
      background-size: cover;
    }
  }
  @media only screen
  and (max-width:768px)
  and (device-height : 667px){
    .mainTitle{
      font-size: 1.75rem;
    }
    .mainContent{
      .content{
        font-size: 0.85rem;
      }
    }
  }
</style>
