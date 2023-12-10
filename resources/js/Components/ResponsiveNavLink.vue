<script setup>
import { computed } from 'vue';
import { Link } from '@inertiajs/vue3';

const props = defineProps({
    href: {
        type: String,
        required: true,
    }
});

</script>

<template>
    <Link :href="href" class="group flex w-full items-center rounded-md px-2 py-2 text-sm gap-2 hover:bg-violet-500 hover:text-white">
        <slot />
    </Link>
</template>
