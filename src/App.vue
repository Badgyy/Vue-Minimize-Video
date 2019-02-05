<template>
  <v-app dark>
    <router-view></router-view>
    <div v-if="!notVideoView" class="float-lower-left">
      <router-link to="/videoview">
      <keep-alive>
        <videoplayer-component></videoplayer-component>
      </keep-alive>
      </router-link>
    </div>
  </v-app>
</template>

<script>
import VideoplayerComponent from '@/components/VideoplayerComponent'

export default {
  name: 'App',
  components: { VideoplayerComponent },
  data () {
    return {
      //
    }
  },
  computed: {
     notVideoView () {
       return this.$route.path === '/videoview' ? true : false
     }
  }
}
</script>
<style lang="scss">
.float-lower-left {
     position:absolute;
     bottom:0;
     right:0;
}
</style>

