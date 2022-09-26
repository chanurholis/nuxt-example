<template>
    <MainLayout>
        <h1>Login Page</h1>
    </MainLayout>
</template>

<script lang="ts">
import Vue from 'vue';

import MainLayout from '~/layouts/public/MainLayout.vue';

export default Vue.extend({
    name: "LoginContainer",
    components: { MainLayout },
})
</script>