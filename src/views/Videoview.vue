<template>
    <div id="videoview">
        <v-container>
            <keep-alive>
                <videoplayer-component></videoplayer-component>
            </keep-alive>

            <router-link to="/">Home</router-link>
        </v-container>
    </div>
</template>
<script>
import VideoplayerComponent from '@/components/VideoplayerComponent'
export default {
    components: { VideoplayerComponent }
}
</script>
