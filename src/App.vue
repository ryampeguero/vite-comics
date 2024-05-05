<script>
import AppHeader from "./components/AppHeader.vue";
import AppHero from "./components/AppHero.vue";
import AppCard from "./components/AppCard.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

//JSON File
import jsonData from "./assets/data/dc-comics.json";

export default {
    components: {
        AppHeader,
        AppHero,
        AppCard,
        AppMain,
        AppFooter,
        jsonData
    },

    data(){
        return {
            realData: jsonData
        }
    },

    created(){
        console.warn(jsonData);
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
        <AppCard />
    </section>

    <section>
        <AppMain />
    </section>
    
    <section>
        <AppFooter />
    </section>
</template>

<style lang="scss">

</style>