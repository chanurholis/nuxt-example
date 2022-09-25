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
import HeaderLayout from './HeaderLayout.vue';
import FooterLayout from './FooterLayout.vue';

export default {
    name: "MainLayout",
    components: { HeaderLayout, FooterLayout }
}
</script>