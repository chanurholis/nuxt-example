<template>
    <div>
        <HeaderLayout/>
        <div class="container mx-auto p-6">
            <slot />
        </div>
        <FooterLayout/>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';

import HeaderLayout from './HeaderLayout.vue';
import FooterLayout from './FooterLayout.vue';

export default Vue.extend({
    name: "MainLayout",
    components: { HeaderLayout, FooterLayout }
})
</script>