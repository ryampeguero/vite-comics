<script>
export default {
    data() {
        return {
            navItems: [
                {
                    itemName: "CHARACTERS",
                    isActive: false,
                },
                {
                    itemName: "COMICS",
                    isActive: true,
                },
                {
                    itemName: "MOVIES",
                    isActive: false,
                },
                {
                    itemName: "TV",
                    isActive: false,
                },
                {
                    itemName: "GAMES",
                    isActive: false,
                },
                {
                    itemName: "COLLECTIBLES",
                    isActive: false,
                },
                {
                    itemName: "VIDEOS",
                    isActive: false,
                },
                {
                    itemName: "FANS",
                    isActive: false,
                },
                {
                    itemName: "NEWS",
                    isActive: false,
                },
                {
                    itemName: "SHOP",
                    isActive: false,
                },
            ]
        }
    }

}
</script>

<template>
    <div class="navbar">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div class="nav-items">
            <ul>
                <li v-for="currItem in navItems" :class="(currItem.isActive) ? 'active' : ''"><a href="">{{ currItem.itemName }}</a></li>
            </ul>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixin.scss" as *;
@use "../style/partials/variables.scss" as *;

.navbar {
    @include flex(row, space-around, center);
    // padding: 10px;
    min-height: $navHeight;
    // width: 100%;
    margin: 0;

    // debug
    // border: 1px solid black;
    background-color: white;

    .nav-items {
        font-size: 0.8rem;
        font-weight: 600;
        // border: 1px solid grey;
        ul {
            @include flex(row, center, center);

            list-style: none;
            gap: 5px;

            .active {
                border-bottom: 4px solid #0c7cec;
                color: #0c7cec;
            }

            li {
                @include flex(row, center, center);
                padding: 10px;
                min-height: $navHeight;
                // debug
                // border: 1px solid red;
                // Stile addizionale degli li nel navbar

                &:hover {
                    border-bottom: 4px solid #0c7cec;
                }

                a {
                    text-decoration: none;
                    text-align: center;
                    color: black;
                }
            }

        }

    }

    .logo {
        @include flex(row, center, center);

        img {
            width: 3rem;
            aspect-ratio: 1;
        }
    }


}
</style>