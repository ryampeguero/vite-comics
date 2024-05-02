<script>
export default {
    data() {
        return {
            topFooterItems: [
                [ //DC COMICS LIST
                    {
                        itemName: "DC COMICS",
                        isTitle: true,
                    },
                    {
                        itemName: "Characters",
                        isTitle: false,
                    },
                    {
                        itemName: "Comics",
                        isTitle: false,
                    },
                    {
                        itemName: "Movies",
                        isTitle: false,
                    },
                    {
                        itemName: "TV",
                        isTitle: false,
                    },
                    {
                        itemName: "Games",
                        isTitle: false,
                    },
                    {
                        itemName: "Videos",
                        isTitle: false,
                    },
                    {
                        itemName: "News",
                        isTitle: false,
                    },
                ],
                [//SHOP ITEM LIST
                    {
                        itemName: "SHOP",
                        isTitle: true,
                    },
                    {
                        itemName: "Shop DC",
                        isTitle: false,
                    },
                    {
                        itemName: "Shop DC Collectibles",
                        isTitle: false,
                    },
                ],
                [//DC ITEMS LIST
                    {
                        itemName: "DC",
                        isTitle: true,
                    },
                    {
                        itemName: "Terms Of Use",
                        isTitle: false,
                    },
                    {
                        itemName: "Privacy policy (New)",
                        isTitle: false,
                    },
                    {
                        itemName: "Ad Choices",
                        isTitle: false,
                    },
                    {
                        itemName: "Advertising",
                        isTitle: false,
                    },
                    {
                        itemName: "Jobs",
                        isTitle: false,
                    },
                    {
                        itemName: "Subscriptions",
                        isTitle: false,
                    },
                    {
                        itemName: "Talent Workshops",
                        isTitle: false,
                    },
                    {
                        itemName: "CPSC Certificates",
                        isTitle: false,
                    },
                    {
                        itemName: "Ratings",
                        isTitle: false,
                    },
                    {
                        itemName: "Shop Help",
                        isTitle: false,
                    },
                    {
                        itemName: "Contact Us",
                        isTitle: false,
                    },
                ],
                [ //SITES ITEM LIST
                    {
                        itemName: "SITES",
                        isTitle: true,
                    },
                    {
                        itemName: "DC",
                        isTitle: false,
                    },
                    {
                        itemName: "MAD Magazine",
                        isTitle: false,
                    },
                    {
                        itemName: "DC Kids",
                        isTitle: false,
                    },
                    {
                        itemName: "DC Universe",
                        isTitle: false,
                    },
                    {
                        itemName: "DC Power Visa",
                        isTitle: false,
                    },
                ]
            ],

            bottomFooterIcons: [
                {
                    imgPath: "footer-facebook.png"
                },
                {
                    imgPath: "footer-twitter.png"
                },
                {
                    imgPath: "footer-youtube.png"
                },
                {
                    imgPath: "footer-pinterest.png"
                },
                {
                    imgPath: "footer-periscope.png"
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
    <div class="top-Footer">
        <div class="left-Items">
            <ul v-for="title in topFooterItems">
                <li v-for="currItem in title"><a href="" :class="(currItem.isTitle) ? 'title' : ''">{{
                    currItem.itemName }}</a></li>
            </ul>
        </div>

        <div class="dc-logo">

        </div>
    </div>

    <div class="bottom-Footer">
        <button class="sign-btn">
            SIGN-UP NOW!
        </button>

        <div class="social">
            <div class="follow">FOLLOW US</div>
            <ul>
                <li v-for="currItem in bottomFooterIcons">
                    <a href="">
                        <img :src="getImgItem(currItem.imgPath)" alt="">
                    </a>
                </li>

            </ul>
        </div>
    </div>
</template>

<style lang="scss">
@use "../style/partials/mixin.scss" as *;
@use "../style/partials/variables.scss" as *;

// @include flex(row, center, center);


.top-Footer {
    @include flex(row, flex-start, center);
    position: relative;
    min-height: $topFooter;
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    background-repeat: no-repeat;

    .left-Items {
        @include flex(column, center, flex-start);
        flex-wrap: wrap;
        gap: 5px;
        max-height: $topFooter;
        margin: 0 40px;
        padding: 0 40px;
        // debug
        // border: 1px solid white;

        .title {
            font-size: 1.2rem;
            font-weight: 600;
            color: white;
        }

        ul {
            list-style: none;
            flex-grow: 1;
            padding: 10px 20px;

            li {
                font-size: 0.6rem;

                a {
                    text-decoration: none;
                    text-align: center;
                    color: grey;

                    &:hover {
                        border-bottom: 1px solid grey;
                    }
                }
            }
        }
    }

    .dc-logo {
        position: absolute;
        top: -90px;
        // left: 30;
        right: 100px;
        background-image: url("../assets/img/dc-logo-bg.png");
        background-repeat: no-repeat;
        background-position: center;
        background-size: contain;
        min-width: 380px;
        aspect-ratio: 1;

        z-index: 10;
        // border: 1px solid white;
    }
}

.bottom-Footer {
    @include flex(row, space-between, center);
    position: relative;
    min-height: $bottomFooter;
    background-color: $bottomFooterColor;
    z-index: 100;

    .sign-btn {
        margin: 0 40px;
        padding: 10px;
        background-color: inherit;
        color: white;
        border: 3px solid $headerLogoColor;


        &:hover {
            border: 3px solid white;
        }
    }

    .social {
        @include flex(row, space-around, center);

        margin: 0 40px;
        width: 40%;

        div {
            color: $mainColor;
            font-weight: 700;
        }


        ul {
            @include flex(row, center, center);
            list-style: none;
            gap: 15px;
            li {
                
                a {
                    text-decoration: none;
                    text-align: center;
                    
                    img {
                        width: 30px;
                        aspect-ratio: 1;
                    }
                }
            }
        }


    }
}
</style>