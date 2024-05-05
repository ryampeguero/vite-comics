<script>
export default {

    data() {

    }
}
</script>

<template>
    <div class="hero container">
        <div class="content"></div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin.scss" as *;
@use "../style/partials/variables.scss" as *;

.hero {
    @include flex(row, flex-start, center);

    min-height: $heroHeight;
    max-width: $heroWidth;
    background-color: #1C1C1C;
    color: white;
    // padding: 0px 20px;

    background-image: url("../assets/img/jumbotron.jpg");

    background-repeat: no-repeat;
    background-size: cover;

    .content {
        max-width: 100%;
        // debug
        // border: 1px solid white;

    }

}
</style>