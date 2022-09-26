<template>
    <LoginContainer />
</template>

<script lang="ts">
import Vue from 'vue';

import LoginContainer from '~/containers/LoginContainer.vue';

export default Vue.extend({
    name: "LoginPage",
    components: { LoginContainer }
})
</script>