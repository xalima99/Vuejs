<template>
    <div class="col-md-4 ml-auto">
        <ul class="list-group">
            <VideoListItem v-for="video in videos" 
            @videoSelect="onVideoSelect"
            :video="video"
            :key="video.etag">
            </VideoListItem>
        </ul>
    </div>
</template>

<script>
import VideoListItem from './videoListItem';

export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    methods: {
        onVideoSelect(video) {
            this.$emit('videoSelect', video)
        }
    },
    props: {
        videos: Array
    }
}
</script>

<style lang="stylus" scoped>

</style>