<template>
  <div class="container text-center d-flex justify-content-center">
    <div class="card-group">
      <div
        v-for="article in info"
        :key="article.id"
        class="card bg-dark text-light"
        style="width: 20em;"
      >
        <a :href="article.url" target="_blank" class="text-light">
          <div>
            <img
              :src="getImage(article.contents.split(' ')[0])"
              class="card-img-top"
            />
          </div>
          <div class="card-body">
            <h5 class="card-title">{{ article.title }}</h5>
            <p class="card-text">
              {{ article.contents.split(".png")[1] }}
            </p>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
// import axios from "axios";
import artifact from "@/assets/json/artifact.json";

export default {
  data() {
    return {
      info: artifact.appnews.newsitems,
    };
  },
  // mounted() {
  //   axios
  //     .get('../public/json/artifact.json')
  //     .then((response) => (this.info = response.data.appnews.newsitems));
  // },
  methods: {
    getImage(str) {
      let newStr = str.replace(
        "{STEAM_CLAN_IMAGE}",
        "https://steamcdn-a.akamaihd.net/steamcommunity/public/images/clans"
      );
      return newStr;
    },
  },
  computed: {},
};
</script>

<style scoped></style>
