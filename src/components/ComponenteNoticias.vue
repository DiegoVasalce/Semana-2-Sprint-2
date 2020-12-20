<template>
  <div class="row mt-5">
    <div
      class="col-lg-6 col xs-12 card-group"
      v-for="(anime, index) of result"
      v-bind:key="index"
    >
      <div class="card m-2 text-white bg-secondary mb-3">
        <div class="card-header">
          <h5 class="text-center">
            <b>{{ anime.attributes.canonicalTitle }}</b>
          </h5>
        </div>
        <img
          class="card-img-top p-2"
          v-bind:src="anime.attributes.posterImage.small"
          alt="PosterImg"
          height="400"
        />
        <!-- <h5>{{anime.attributes.posterImage.medium}}</h5> -->
        <div class="card-body">
          <!-- <h5 class="card-title"></h5> -->
          <p class="card-text text-justify">
            {{ anime.attributes.description }}
          </p>
        </div>
        <button type="button" class="btn btn-dark">
          <a
            v-bind:href="
              'https://www.google.com/search?q=' +
              anime.attributes.canonicalTitle
            "
            class="text-white"
            target="_blank"
          >
            Mas info..</a
          >
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "ComponenteNoticias",
  data() {
    return {
      result: Object,
      anime: Object,
    };
  },
  mounted() {
    axios.get("https://kitsu.io/api/edge/manga ").then((response) => {
      this.result = response.data.data.slice(0, 4);
    });
  },
};
</script>

<style scoped>
</style>