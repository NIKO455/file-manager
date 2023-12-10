<script setup>
import TextInput from "@/Components/TextInput.vue";
import {useForm} from "@inertiajs/vue3";

const form = useForm({
    search: ''
})
</script>

<template>
    <form class="w-[600px] h-[80px] flex items-center">
        <label for="default-search"
               class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white">Search</label>
        <div class="relative">
            <div class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none">
                <svg class="w-4 h-4 text-gray-500 dark:text-gray-400" aria-hidden="true"
                     xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 20">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                          d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"/>
                </svg>
            </div>
            <TextInput type="search" id="default-search"
                   class="block w-[45vw] p-3 ps-10 text-sm border border-gray-300 rounded-lg bg-gray-50  dark:border-gray-600 dark:placeholder-gray-400 dark:text-black"
                   placeholder="Search for files and folder" required v-model="form.search" autocomplete>
            </TextInput>
            <button type="submit"
                    class="text-white absolute end-2 bottom-1.5 bg-violet-700 hover:bg-violet-800 focus:outline-none focus:ring-violet-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-violet-600 dark:hover:bg-violet-700 dark:focus:ring-violet-800">
                Search
            </button>
        </div>
    </form>
</template>

<style scoped>

</style>
