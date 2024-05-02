<script>
export default {
    data() {

        return {
            mainItems: [
                {
                    itemName: "DIGITAL COMICS",
                    iconUrl: "buy-comics-digital-comics.png",
                },
                {
                    itemName: "DC MERCHANDISE",
                    iconUrl: "buy-comics-merchandise.png"
                },
                {
                    itemName: "SUBSCRIPTION",
                    iconUrl: "buy-comics-subscriptions.png"
                },
                {
                    itemName: "COMIC SHOP LOCATOR",
                    iconUrl: "buy-comics-shop-locator.png"
                },
                {
                    itemName: "DC POWER VISA",
                    iconUrl: "buy-dc-power-visa.svg"
                },

            ]
        }
    },

    methods: {
        getImgItem(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="content">
        <ul>
            <li v-for="currItem in mainItems"><a href=""><img :src="getImgItem(currItem.iconUrl)"
                        :class="(currItem.iconUrl === 'buy-comics-shop-locator.png') ? 'locator' : ''"></img>{{
                            currItem.itemName }}</a></li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin.scss" as *;
@use "../style/partials/variables.scss" as *;

.content {
    background-color: $mainColor;
    min-height: $mainHeight;
    color: white;

    ul {
        @include flex(row, center, center);

        list-style: none;
        gap: 5px;

        li {
            @include flex(row, center, center);

            padding: 10px;
            min-height: $mainHeight;
            // debug
            // border: 1px solid red;

            // Stile addizionale degli li nel Main

            a {
                @include flex(row, center, center);

                text-decoration: none;
                text-align: center;
                color: white;
                gap: 5px;

                img {
                    width: 30px;
                }

                .locator {
                    max-width: 22px;
                    // max-height: 10px;
                }
            }
        }

    }
}
</style>