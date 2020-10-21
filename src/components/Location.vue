<template>
  <!-- <v-main padding="0"> -->
    <!-- Provides the application the proper gutter -->
    <v-container fluid pa-0 >
      <div class="pointUp"></div>
      <div class="bottomView" id="location">
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
                <!-- <GMap
                v-if="!isLoading"
                :center="{lat, lng}"
                :restaurants="restaurants"
                :streetViewControl="false"
                :mapTypeControl="false"
                :fullscreenControl="true"
                :zoomControl="true"
                :zoom="17"
              ></GMap> -->
                <img src="../assets/map2.png"/>
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
                  <!-- <li>
                    <p>{{ information[3].title }}</p>
                    <span>{{ information[3].text }}<img src="../assets">{{ information[3].url }}</img></span>
                  </li> -->
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
// 載入 GMap Component
// import GMap from './Gmap.vue'
export default {
  name: 'Location',
  components: {
    // GMap
  },
  data () {
    return {
      information: [
        { title: 'Address', text: '台中市北區漢口路三段168-2號' },
        { title: 'Phone Number', text: '(04)2298-9828 | 0938-780508' },
        { title: 'Opening', text: '早 11:00 - 14:00 | 晚 17:00 - 20:00' },
        { title: 'Social', text: '粉絲團', url: 'https://reurl.cc/WLb4ve' }
      ],
      lat: 24.166877,
      lng: 120.671597,
      restaurants: []
    }
  },
  methods: {
  }
}
</script>
<style lang="scss" scoped>
  $color_word: #faecb9;
  $color_main: #729ea1;
  .google-map {
  width: 100%;
  height: 35vh;
  }
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
              // border: 2px solid $color_main;
              object-fit: contain;
              // box-shadow: 10px 10px 40px 10px $color_main;
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
  @media only screen and (max-width:1024px){
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
      // padding-top: 5vh;
      ul{
        padding: 0;
        li{
          font-size: 1.5rem!important;
          p{
            font-size: 16px;
          }
        }
      }
    }
    .mainContent{
      display: inline-block!important;
    }
  }
  @media only screen and (max-width:768px){
    .information{
      // padding-top: 5vh;
      font-size: .9rem;
      ul{
        padding: 0;
        li{
          font-size: 1rem!important;
        }
      }
    }
    .bottomView{
      .contactUs{
        padding:  25px 50px;
      }
    }
  }
  @media only screen
  and (max-width:375px)
  and (device-height : 667px){
    .information{
      // padding-top: 5vh;
      ul{
        padding: 0;
        li{
          font-size: .95rem!important;
        }
      }
    }
  }
</style>
