<template>
    <div class="my-10 lg:w-full lg:mt-32 mx-10 p-3 flex flex-col items-center justify-center">
        <input
            type="text"
            v-model="searchInput"
            class="
                block
                text-gray-700
                border border-gray-500
                w-full
                md:text-2xl
                lg:max-w-lg
                py-2
                px-5
                rounded-full
                focus:outline-none
                focus:ring focus:ring-blue-200
            "
            :placeholder="placeholder"
        />
        <Button
            @click="searchGIF"
            text="Search"
            class="
                my-5
                md:text-xl
                border-white
                text-white
                bg-blue-400
                hover:bg-blue-600
                active:bg-blue-400
                transform
                active:scale-90
            "
        />
    </div>
</template>

<script>
import Button from "./Button.vue";

export default {
    name: "InputBox",
    components: {
        Button,
    },
    props: {
        placeholder: {
            type: String,
            default: "",
        },
    },
    data() {
        return {
            searchInput: "",
        };
    },
    methods: {
        searchGIF() {
            console.log("search: " + this.searchInput);
        },
    },
};
</script>
