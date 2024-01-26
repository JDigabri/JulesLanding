<template>
    <NavBar />
    <HeroSection />
    <ButtonSection />
    <MainSection />
    <CardSection />
    <BottomHero />
</template>

<script>

import NavBar from '@/components/NavBar.vue';
import HeroSection from '@/components/HeroSection.vue';
import ButtonSection from '@/components/ButtonSection.vue';
import MainSection from '@/components/MainSection.vue';
import CardSection from '@/components/CardSection.vue';
import BottomHero from '@/components/BottomHero.vue';
import FooterView from '@/components/FooterView.vue';

export default {
    name: 'App', // assuming this is your root component

    mounted() {
        // Disable horizontal scrollbar when the component mounts
        document.body.style.overflowX = 'hidden';
    },

    beforeUnmount() {
        // Re-enable horizontal scrollbar when the component is about to unmount
        document.body.style.overflowX = '';
    },

    components: {
        NavBar,
        HeroSection,
        ButtonSection,
        MainSection,
        CardSection,
        BottomHero,
        FooterView
    }
}

</script>


<style>
body{
    overflow-x: hidden !important;
    width: 100vw;
    max-width: 100vw !important;


}
</style>