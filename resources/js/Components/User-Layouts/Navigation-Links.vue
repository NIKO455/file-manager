<script setup>
import {Link} from "@inertiajs/vue3";
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import CreateNewDropdonw from "@/Components/User-Layouts/CreateNewDropdown.vue";
import NavLink from "@/Components/NavLink.vue";
</script>

<template>
    <nav class="min-w-[200px]">
        <div class="h-[80px] px-3 flex items-center gap-3">
            <Link :href="route('myfiles')">
                <ApplicationLogo
                    class="block h-9 w-auto fill-current text-gray-800"
                />
            </Link>
            StoreLara
        </div>
        <div class="px-3">
            <CreateNewDropdonw/>
            <div class="py-3">
                <NavLink :href="route('myfiles')" :active="true">My Files</NavLink>
                <NavLink href="/">Sent Files</NavLink>
                <NavLink href="/">Received Files</NavLink>
                <NavLink href="/">Trash Files</NavLink>
            </div>
        </div>
    </nav>
</template>

<style scoped>

</style>
