<template>
    <div>
        <h1>videos</h1>
        <div v-for="video in videos" :key="video.id">
            <nuxt-link :to="`/videos/${video.id}`">{{ video.name }} </nuxt-link>
        </div>
    </div>
</template>

<script>
    export default {
       async asyncData($axios){
            let response = await $axios.get('/videos')
            let videos = response.data.data.videos;
            return{
                videos
            }

        }
        
    }
</script>

<style lang="scss" scoped>

</style>