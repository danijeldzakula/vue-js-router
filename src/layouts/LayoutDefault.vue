<template>
    <div class="layout">
      <NavBar />
      <main class="main">
        <slot />
      </main>
      <FooterBar />
    </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import FooterBar from '@/components/FooterBar.vue';

export default {
  name: 'LayoutDefault',
  components: {
    NavBar,
    FooterBar
  }
}
</script>