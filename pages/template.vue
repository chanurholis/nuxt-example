<template>
    <div class="container p-8">
        <h1 class="text-center py-2 font-bold">Template</h1>
        <br>
        <div>
            <h2>Button</h2>
            <ButtonComponent name="Primary" type="primary" />
            <ButtonComponent name="Success" type="success" />
            <ButtonComponent name="Secondary" type="secondary" />
            <ButtonComponent name="Warning" type="warning" />
            <ButtonComponent name="Danger" type="danger" />
            <ButtonComponent name="Default" />
        </div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';

import ButtonComponent from '~/components/ButtonComponent.vue';

export default Vue.extend({
    name: "TemplatePage",
    components: { ButtonComponent }
})
</script>