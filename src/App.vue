<template>
  <div id="app">
    <div id="nav">
      <Navbar />
    </div>
    <div id="main-view" class="mb-5 pb-5">
      <router-view />
    </div>
    <Socials />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Socials from "@/components/Socials.vue";

export default {
  components: {
    Navbar,
    Socials,
  },
  mounted() {
    this.createTitle();
  },
  methods: {
    createTitle() {
      document.title =
        "Brainscans.net | Competitive & Inclusive Artifact Tournaments";
    },
  },
};
</script>
<style>
html body {
  background-color: #1d1025;
  color: white;
}
</style>
