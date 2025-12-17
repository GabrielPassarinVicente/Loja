<template>
    <div>
        <AppNavbar/>
        <div class="main-content">
            <Nuxt />
        </div>
       
    </div>
</template>
<script>
    import AppNavbar from '~/components/AppNavbar.vue';
    export default {
        components: {
            AppNavbar
        }
    }
</script>
<style>
    body{
        background-color: #f8f9fa;
    }
</style>
