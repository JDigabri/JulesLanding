<template>
    <NavBar />
    <HeroSection />
    <ButtonSection />
    <MainSection />
</template>

<script>

import NavBar from '@/components/NavBar.vue';
import HeroSection from '@/components/HeroSection.vue';
import ButtonSection from '@/components/ButtonSection.vue';
import MainSection from '@/components/MainSection.vue';

export default {
    components: {
        NavBar,
        HeroSection,
        ButtonSection,
        MainSection,
    }
}

</script>
