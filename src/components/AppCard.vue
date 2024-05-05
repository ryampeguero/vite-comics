<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="container">
        <div class="card">
            ciao
        </div>
    </div>
</template>

<style lang="scss">
@use "../style/partials/mixin.scss" as *;
@use "../style/partials/variables.scss" as *;

// @include flex(row, center, center);

.container {

    .card {
        width: 60px;
        height: 60px;
        margin: 20px;
        // debug
        border: 2px solid white;
    }
}
</style>