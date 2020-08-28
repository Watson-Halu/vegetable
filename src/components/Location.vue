<template>
  <!-- <v-main padding="0"> -->
    <!-- Provides the application the proper gutter -->
    <v-container fluid pa-0 >
      <div class="pointUp"></div>
      <div class="bottomView" ref="location">
        <div class="contactUs">
          <h1>
            <span class="mainTitle">找到食堂</span>
          </h1>
          <span class="subTitle">
            Location
          </span>
          <div class="mainContent">
            <div class="leftSide">
              <div class="map">
                <img src="../assets/location.png"/>
              </div>
            </div>
            <div class="rightSide">
              <div class="information">
                <ul>
                  <li>
                    <p>{{ information[0].title }}</p>
                    <span>{{ information[0].text }}</span>
                  </li>
                  <li>
                    <p>{{ information[1].title }}</p>
                    <span>{{ information[1].text }}</span>
                  </li>
                  <li>
                    <p>{{ information[2].title }}</p>
                    <span>{{ information[2].text }}</span>
                  </li>
                </ul>
              </div>
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
  name: 'Location',

  data () {
    return {
      information: [
        { title: 'Address', text: '台中市山西路xxxxxxxxxxxx' },
        { title: 'Phone Number', text: '(04)1234-5678' },
        { title: 'Opening', text: '11:00 - 20:00' }
      ]
    }
  },
  methods: {
  }
}
</script>
<style lang="scss" scoped>
  $color_word: #faecb9;
  $color_main: #729ea1;
  .pointUp{
    width: 0;
    height: 15vh;
    border-style: solid;
    border-width: 0 50vw 15vh 50vw;
    border-color: transparent transparent $color_main transparent;
    position: absolute;
    bottom: 100vh;
  }
  .bottomView{
    height:100vh;
    background: linear-gradient(to bottom,$color_main, #435d5f );
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center center;
    padding-top: 10vh;
    .contactUs{
      text-align: center;
      background-color: rgba(255,255,255,0.5);
      padding: 50px;
      margin: 2vh 10% 5vh 10%;
      h1{
        .mainTitle{
          border-bottom: 2px solid #000;
        }
        .subTitle{
          display: block;
          color: $color_word;
        }
      }
      .mainContent{
        display: flex;
        margin-top: 5vh;
        .leftSide{
          width: 100%;
          text-align: right;
          .map {
            img{
              width: 100%;
              height: 35vh;
              border: 2px solid $color_main;
              object-fit: cover;
              box-shadow: 10px 10px 40px 10px $color_main;
            }
          }
        }
        .rightSide{
          width: 100%;
        }
      }
      .information{
        text-align: center;
        ul{
          list-style: none;
          li{
            margin-bottom: 3vh;
            font-size: 1.1rem;
            font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
            p{
              font-weight: bolder;
            }
          }
        }
      }
    }
  }
  @media screen and (max-width:1024px){
    .pointUp{
      bottom: 120vh;
      border-width: 0 50vw 8vh 50vw;
    }
    .bottomView{
      position: relative;
      bottom: 10vh;
      height: 110vh;
      margin:0;
      .contactUs{
        margin: 0;
      }
    }
    .information{
      padding-top: 5vh;
      ul{
        padding: 0;
        li{
          font-size: 1.5rem!important;
        }
      }
    }
    .mainContent{
      display: inline-block!important;
    }
  }
  @media screen and (max-width:768px){
    .information{
      padding-top: 5vh;
      ul{
        padding: 0;
        li{
          font-size: 1.2rem!important;
        }
      }
    }
  }
</style>
