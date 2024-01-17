<template>
  <layout-default>
    <router-view/>
  </layout-default>
</template>

<script>
import LayoutDefault from './layouts/LayoutDefault.vue';

export default {
  name: 'App',
  components: {
    LayoutDefault,
  },
  props: {},
  computed: {},
  methods: {},  
}
</script>

<style lang="scss">
@use '@/assets/scss/abstracts/variables' as *;
</style>
