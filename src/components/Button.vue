<template>
    <button class="font-semibold focus:outline-none border-2 py-2 px-5 rounded-full">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: "Button",
    props: {
        text: {
            type: String,
            default: " ",
        },
        priColor: {
            type: String,
            default: "white",
        },
        secColor: {
            type: String,
            default: "black",
        },
    },
};
</script>
