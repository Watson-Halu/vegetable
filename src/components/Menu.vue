<template>
  <!-- <v-main padding="0"> -->
    <!-- Provides the application the proper gutter -->
    <v-container fluid pa-0>
      <!-- 做出三角形連接 -->
      <div class="connectTopLeft"></div>
      <div class="connectTopRight"></div>
      <!-- 主內容 -->
      <div class="middleView"  id="menu">
        <div class="menuText">
          <span class="menuTitle">
            素說菜單
          </span>
          <span class="subTitle">
            Menu
          </span>
          <ul v-for='menu of menus' :key='menu.nameCN'>
            <li >
              <span class="liLeft">
                <span>
                <img class="crown" src="../assets/crown.png"/>
                </span>
                {{ menu.nameCN }}<br>
                {{ menu.nameEN }}
              </span>
              <span class="liright">··· ${{ menu.price }}</span>
            </li>
          </ul>
        </div>
      </div>
      <!-- 做出三角形連接 -->
      <div class="connectBottomLeft"></div>
      <div class="connectBottomRight"></div>
      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  <!-- </v-main> -->

  <!--<v-footer app>
  </v-footer>-->
</template>

<script>
export default {
  name: 'Menu',
  data () {
    return {
      menus: [
        // 主要放推薦的7個
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 },
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 },
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 },
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 },
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 },
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 },
        { nameCN: '蕈菇義大利麵', nameEN: 'Mushroom spaghetti', price: 120 }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
  $color_word: #faecb9;
  $color_main: #729ea1;
  .connectTopLeft{
    height: 15vh;
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 0 0 15vh 50vw;
    border-color: transparent transparent $color_main transparent;
    position: absolute;
    left: 50vw;
    top: 85vh;
  }
  .connectTopRight{
    height: 15vh;
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 15vh 0 0 50vw;
    border-color: transparent transparent transparent $color_main ;
    position: absolute;
    top: 85vh;
  }
  .connectBottomLeft{
    height: 15vh;
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 0 50vw 15vh 0;
    border-color: transparent $color_main transparent transparent;
    position: absolute;
    left: 0;
    bottom: 195vh;
  }
  .connectBottomRight{
    height: 15vh;
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 15vh 50vw 0 0;
    border-color: $color_main transparent transparent transparent;
    position: absolute;
    left: 50vw;
    bottom: 195vh;
  }
  .middleView{
    position: relative;
    top: 0vh;
    height: 100vh;
    background-color: $color_main;
    background-image: url('../assets/menuBG.png');
    background-position: center center;
    background-size: 90% 100%;
    text-align: center;
    padding: 10vh 5% 0 5%;
    .menuTitle{
      font-size: 2rem;
      color: $color_word;
      border-bottom: 2px solid $color_word;
    }
    .subTitle{
      display: block;
      color: $color_word;
    }
    ul{
      padding: 2vh 35% 0 30%;
      color: $color_word;
      font-size: 1.1rem;
      li{
        display: flex;
        justify-content: space-between;
        margin-top: 1vh;
        font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        .crown{
          width: 10%;
          transform: scale(2.5)
        }
      }
      .liLeft{
        width: 100%;
      }
      .liright{
        width: 100%;
      }
    }
  }
  @media only screen and (max-width:1024px){
    .middleView{
      padding: 10vh 5% 0 5%;
      background-size: cover;
      height: 80vh;
      ul{
        padding: 1vh 0 0 0;
        font-size: 1.4rem;
      }
    }
    .connectTopLeft{
      top: 92vh;
      border-width:0 0 8vh 50vw;
    }
    .connectTopRight{
      top: 92vh;
      border-width: 8vh 0 0 50vw;
    }
    .connectBottomLeft{
      bottom: 192vh;
      border-width:0 50vw 8vh 0;;
    }
    .connectBottomRight{
      bottom: 192vh;
      border-width: 8vh 50vw 0 0;
    }
  }
  @media only screen and (max-width:767px){
    .middleView{
      padding: 10vh 5% 0 5%;
      background-size: cover;
      height: 80vh;
      ul{
        padding: 1vh 0 0 0;
        font-size: .85rem;
      }
    }
    .connectBottomLeft{
      bottom: 232vh;
      border-width:0 50vw 8vh 0;;
    }
    .connectBottomRight{
      bottom: 232vh;
      border-width: 8vh 50vw 0 0;
    }
  }
  @media only screen
  and (max-width:375px)
  and (device-height : 667px){
    .menuTitle{
      font-size: 1.75rem!important;
    }
    .middleView{
      padding: 10vh 5% 0 5%;
      background-size: cover;
      height: 80vh;
      ul{
        padding: .5vh 0 0 0;
        font-size: .85rem;
      }
    }
  }

</style>
