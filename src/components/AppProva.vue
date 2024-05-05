<script>
export default {
    props: {
        Cardthumb: String,
        CardSeries: String,
    },

    data() {
        return {

        }
    },

}
</script>

<template>
    <div class="card-container">
        <div class="card">
            <a href="">
                <img :src="Cardthumb" alt="">
                <span>{{ CardSeries }}</span>
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin.scss" as *;
@use "../style/partials/variables.scss" as *;

// @include flex(row, center, center);

.card-container {

    @include flex(row, center, center);
    margin-bottom: 40px;

    .card {
        @include flex(row, center, center, wrap);

        max-width: $cardWidth;
        max-height: $cardHeight;

        margin: 20px;

        // debug
        border: 2px solid white;
        a {
            text-decoration: none;
            text-align: center;
            color: white;
            img {
                min-width: $cardWidth;
                max-width: $cardWidth;

                min-height: $cardHeight;
                max-height: $cardHeight;

            }

            span {
                font-size: 0.6rem;
            }
        }
    }
}
</style>