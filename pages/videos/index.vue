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
        data(){
            return{
                videos:[
                    {
                        id:'1',
                        name:"Introduction to nuxtjs"
                    },
                    {
                        id:'2',
                        name:"Introduction to vue js"
                    },
                    {
                        id:'3',
                        name:"Advanced tuto"
                    }
                ]
            }

        }
        
    }
</script>

<style lang="scss" scoped>

</style>