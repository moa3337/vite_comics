<script>
export default {
    name: "AppFeature",
    props: {
        image: Image,
        name: String,
        price: Number,
    },
};
</script>

<template>
    <div class="feature">
        <div class="feature-icon">
            <img :src="'/images/' + image" :alt="name" />
        </div>
        <p class="feature-name uppercase">
            {{ name }}
        </p>
        <span>{{ price }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.feature {
    @include flexbox(row, center, center);

    .feature-icon {
        width: 55px;
        height: 55px;
        margin-right: 10px;

        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }
}
</style>
