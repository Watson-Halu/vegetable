<template>
  <v-app>
    <v-main padding="0">
       <NavBar/>
      <TopContent/>
    </v-main>
    <v-footer app>
    <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
import TopContent from './components/TopContent'
import NavBar from './components/NavBar'

export default {
  name: 'App',

  components: {
    TopContent,
    NavBar
  },

  data: () => ({
    //
  })
}
</script>
