<template>
    <div class="my-10 lg:w-full lg:mt-32 mx-10 p-3 flex flex-col items-center justify-center">
        <input
            type="text"
            v-model="searchInput"
            @keyup.enter="searchGIF"
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
    import Button from './Button.vue';

    export default {
        name: 'InputBox',
        components: {
            Button,
        },
        props: {
            placeholder: {
                type: String,
                default: '',
            },
        },
        data() {
            return {
                searchInput: '',
                offset: 0,
            };
        },
        methods: {
            async searchGIF() {
                this.offset = 0;

                if (this.searchInput.trim() != '') {
                    let API_key = 'Q0mxSRk57mH7GxZnjGXM5oUKBKdUWraQ';
                    let URL =
                        'https://api.giphy.com/v1/gifs/search?api_key='.concat(API_key) +
                        '&q='.concat(this.searchInput.trim()) +
                        '&limit=10&offset='.concat(this.offset);

                    console.log(URL);
                    const res = await fetch(URL);
                    const results = await res.json();
                    console.log(results);
                } else {
                    console.log('input something');
                }
            },
        },
    };
</script>
