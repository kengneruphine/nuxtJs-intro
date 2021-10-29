<template>
    <div>
        <nuxt-child :video="video" />
    </div>
</template>

<script>
    export default {
        head(){  //making the title dynamic
            return{
                title:'',
                titleTemplate: `%s ${this.video.name} - vue screencast`   //the video is being returned by the function below
            }

        },
        async getVideo($axios, params){
            let response = await $axios.get(`/videos/${params.id}`);
            let video = response.data.data.videos;
            return{
                video
            }

    },
}
    
</script>

<style lang="scss" scoped>

</style>