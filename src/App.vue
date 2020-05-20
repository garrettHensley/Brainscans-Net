<template>
  <div id="app">
    <div id="nav">
      <Navbar />
    </div>
    <router-view />
    <Socials />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Socials from '@/components/Socials.vue';

export default {
  components: {
    Navbar,
    Socials
  }
}
</script>
<style>
html body {
  background-color: #1d1025;
  color: white;
}
</style>
