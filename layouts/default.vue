<template>
    <div>
        <div id="navbar">
            <div class="navbar-links">
                <nuxt-link to="/">Home</nuxt-link>
                <nuxt-link to="/videos">Videos</nuxt-link>
            </div>

        </div>

        <div id="default-body">
            <nuxt />
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

#navbar{
    height:40px;
    width:100%;
    background-color:#333
}

#navbar .navbar-links{
    max-width:800px;
    margin:auto;
}

#navbar a{
    color: white;
    text-decoration: none;
    margin-right: 10px;
}

#default-body{
    max-width:800px;
    margin:auto;
}

</style>