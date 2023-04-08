<script>
import comicsData from "./../data/comicsData";
import featuresData from "./../data/featuresData";

import AppFeature from "./AppFeature.vue";
import AppJumbotron from "./AppJumbotron.vue";
import SingleComic from "./SingleComic.vue";

export default {
    name: "ComicsList",
    data() {
        return {
            features: featuresData,
            comics: comicsData,
        };
    },
    components: {
        AppJumbotron,
        SingleComic,
        AppFeature,
    },
};
</script>

<template>
    <AppJumbotron />

    <section id="current-series" class="dark">
        <div class="container">
            <h2 class="section-title uppercase">Current Series</h2>
            <div class="series-container">
                <div class="series" v-for="(comic, index) in comics">
                    <a href="#">
                        <div class="thumb">
                            <!-- <img :src="comic.thumb" :alt="comic.series"> -->
                        </div>
                        <p class="uppercase">
                            {{ comic.series }}
                        </p>
                    </a>
                </div>
                <!-- <SingleComic
                  v-for="(comic, index) in comics"
                  :key="index"
                  :comic="comic"
                /> -->
                <a href="#" class="button">Load More</a>
            </div>
        </div>
    </section>
    <section id="features">
        <div class="container">
            <div class="features-container">
                <AppFeature v-for="feature in features" :image="feature.image" :name="feature.name"
                    :price="feature.price" />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.series-container {
    @include flexbox(row, space-around, flex-start, wrap);
    padding-bottom: 20px;
}

#features {
    background-color: $main_color;
    color: $main_bg_text_color;

    .features-container {
        @include flexbox(row, space-around, center);
        padding: 50px 0;
    }
}
</style>
