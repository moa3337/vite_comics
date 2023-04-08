<script>
export default {
    name: "SingleComic",
    props: {
        comic: Object,
    },
};
</script>

<template>
    <div class="series">
        <a href="#">
            <div class="thumb">
                <!-- <img :src="comic.thumb" :alt="comic.series"> -->
            </div>
            <p class="uppercase">
                {{ comic.series }}
            </p>
        </a>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.series {
    flex-basis: 180px;
    margin-bottom: 50px;

    .thumb {
        width: 180px;
        height: 180px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center top;
        }
    }

    a {
        color: $dark_section_text_color;

        p {
            margin: 20px 0 0 0;
        }
    }
}
</style>
