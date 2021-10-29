<template>
    <div>
        <h2>
            We are in video {{ video.name }}
            <nuxt-link :to="`/videos/${video.id}/edit`">
                <button>Edit</button>
            </nuxt-link>
        </h2>

    </div>
</template>

<script>
    export default {
       props:['video'],
       head:{
           title:'Watch'
       }
    }
</script>

<style lang="scss" scoped>

</style>