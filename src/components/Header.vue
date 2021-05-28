<template>
    <header class="pt-3 flex content-center justify-end">
        <Button
            text="About"
            class="border-blue-400 text-blue-400 hover:bg-blue-400 hover:text-white"
        />
    </header>
</template>

<script>
import Button from "./Button.vue";

export default {
    name: "Header",
    components: {
        Button,
    },
};
</script>
