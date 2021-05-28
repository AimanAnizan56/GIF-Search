<template>
    <div class="container mx-auto font-poppins bg-purple">
        <Header />
        <div class="flex flex-col lg:flex-row lg-flex-1">
            <Hero />
            <InputBox />
        </div>
    </div>
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import InputBox from "./components/InputBox.vue";

export default {
    name: "App",
    components: {
        Header,
        Hero,
        InputBox,
    },
};
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style></style>
