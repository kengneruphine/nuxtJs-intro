<template>
    <div>
        <nuxt-child :video="video" />
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
        
    },

    computed:{
        video(){
            return this.videos.find(v => v.id == this.$route.params.id )
        }
    }
    }
</script>

<style lang="scss" scoped>

</style>