<script>
export default {
    name: "AppJumbotron"
}
</script>

<template>
    <div class="jumbotron"></div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.jumbotron {
    background-color: $main_color;
    background-image: url('/images/jumbotron.jpg');
    background-position: center top;
    background-size: cover;
    padding: 200px 0;
}
</style>