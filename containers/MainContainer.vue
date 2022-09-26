<template>
    <MainLayout>
        <h1 class="text-center">Landing Page</h1>
    </MainLayout>
</template>

<script lang="ts">
import Vue from 'vue';

import MainLayout from '~/layouts/public/MainLayout.vue';

export default Vue.extend({
    name: "MainContainer",
    components: { MainLayout }
})
</script>