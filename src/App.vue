<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppHero from "./components/AppHero.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
    components: {
        AppHeader,
        AppMain,
        AppHero,
        AppFooter
    },

    data(){
        return {

        }
    }
}
</script>

<template>
    <AppHeader />
    <AppHero />
    <AppMain />
    <AppFooter />
</template>

<style lang="scss">

</style>