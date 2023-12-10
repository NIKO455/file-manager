<script setup>
import Navigation from "@/Components/User-Layouts/Navigation-Links.vue";
import SearchForm from "@/Components/User-Layouts/SearchForm.vue";
import UserSettingDropdown from "@/Components/User-Layouts/UserSettingDropdown.vue";

</script>

<template>
    <div>
        <div class="flex bg-gray-100 min-h-screen">
            <Navigation/>

            <main class="flex flex-col flex-1 px-4 overflow-hidden">
                <div class="flex items-center justify-between w-full">
                    <SearchForm/>
                    <UserSettingDropdown/>
                </div>
                <div class="flex flex-1 flex-col overflow-hidden">
                    <slot/>
                </div>
            </main>

        </div>
    </div>
</template>
