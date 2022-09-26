<template>
    <div class="text-center">
        <h1 v-if="error.statusCode === 404" class="py-5">Page not found</h1>
        <h1 v-else>An error occurred</h1>
        <NuxtLink to="/" class="hover:text-red-900">Home page</NuxtLink>
    </div>
</template>

<script>
import Vue from 'vue';

export default Vue.extend({
    props: ['error'],
    layout: 'error' // you can set a custom layout for the error page
})
</script>