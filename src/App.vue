<script>
import AppHeader from "./components/AppHeader.vue";
import AppHero from "./components/AppHero.vue";
import AppProva from "./components/AppProva.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

//JSON File
import jsonData from "./assets/data/dc-comics.json";

export default {
    components: {
        AppHeader,
        AppHero,
        AppProva,
        AppMain,
        AppFooter,
        jsonData
    },

    data() {
        return {
            realData: jsonData,
            prova: {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel"
            },
            newArrayObject: [],
        }
    },

    created() {
        console.warn(jsonData, typeof jsonData);

        jsonData.forEach((currItem) => {
            this.newArrayObject.push(currItem);
        });

        console.log(this.newArrayObject);
    }
}
</script>

<template>
    <section>
        <AppHeader />
    </section>

    <section>
        <AppHero />
    </section>

    <section>
        <div class="container flex-wrap">
            <AppProva v-for="currItem in newArrayObject" :Cardthumb="currItem.thumb" :CardSeries="currItem.series" />
        </div>
    </section>

    <section>
        <AppMain />
    </section>

    <section>
        <AppFooter />
    </section>
</template>

<style lang="scss"></style>