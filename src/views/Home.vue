<template>
  <v-app>
    <v-main padding="0">
      <NavBar/>
      <TopContent/>
      <Menu/>
      <Begin/>
      <Location/>
    </v-main>
    <v-footer
      absolute
      class="font-weight-medium"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        &copy;{{ new Date().getFullYear() }} — <strong>素說食堂</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
// @ is an alias to /src
// import MainContent from '@/components/MainContent.vue'
// import NavBar from '@/components/NavBar.vue'
import TopContent from '../components/TopContent'
import Menu from '../components/Menu'
import Begin from '../components/Begin'
import Location from '../components/Location'
import NavBar from '../components/NavBar'
export default {
  name: 'Home',
  components: {
    TopContent,
    Menu,
    Begin,
    Location,
    NavBar
  }
}
</script>
