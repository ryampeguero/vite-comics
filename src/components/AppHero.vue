<script>
export default {

}
</script>

<template>
    <div class="hero">
        <div class="content">
            <span> --> Content goes here<-- </span>
        </div>

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

    .content {
        margin: 0 80px;
        max-width: 100%;
        // debug
        // border: 1px solid white;

        span {
            font-size: 1.5rem;
        }
    }

}
</style>