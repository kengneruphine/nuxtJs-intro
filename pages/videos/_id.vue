<template>
    <div>
        <nuxt-child :video="video" />
    </div>
</template>

<script>
import {mapState} from 'vuex'
    export default {
        head(){  //making the title dynamic
            return{
                title:'',
                titleTemplate: `%s ${this.video.name} - vue screencast`   //the video is being returned by the function below
            }

        },
        async fetch($axios, params){
            let response = await $axios.get(`/videos/${params.id}`);
            let video = response.data.data.videos;
            
            store.commit('SET_CURRENT_VIDEO', video);

    },
    computed:{
        ...mapState({
            video:'currentVideo'
        })
        
    }
}
    
</script>

<style lang="scss" scoped>

</style>