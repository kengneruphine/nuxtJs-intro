<template>
    <div>
        <h1>videos</h1>
        <div v-for="video in $store.state.videos" :key="video.id">
            <nuxt-link :to="`/videos/${video.id}`">{{ video.name }} </nuxt-link>
        </div>
    </div>
</template>

<script>
    export default {
        head:{
            title: "Videos List"
        },
       async fetch($axios, store){
            let response = await $axios.get('/videos')
            let videos = response.data.data.videos;

            store.commit('SET_VIDEOS', videos);

        }
        
    }
</script>

<style lang="scss" scoped>

</style>