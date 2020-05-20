<template>
  <div class="home">
    <Placeholder />
    <NewsFeed />
  </div>
</template>

<script>
import Placeholder from "@/components/Placeholder.vue";
import NewsFeed from '@/components/NewsFeed.vue';

export default {
  name: "Home",
  components: {
    Placeholder,
    NewsFeed
  },
};
</script>
<style scoped>
.home {
  height: 100%;
}
</style>
