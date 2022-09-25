<template>
  <MainContainer />
</template>

<script lang="ts">
import Vue from 'vue'

import MainContainer from '~/containers/MainContainer.vue';

export default Vue.extend({
  name: "IndexPage",
  components: { MainContainer }
})
</script>
