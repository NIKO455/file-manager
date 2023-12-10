<script setup>

import ResponsiveNavLink from "@/Components/ResponsiveNavLink.vue";
import {Menu, MenuButton, MenuItem, MenuItems} from "@headlessui/vue";
</script>

<template>
    <Menu as="div" class="relative inline-block text-left">
        <div>
            <MenuButton
                class="flex w-full items-center gap-1 justify-center rounded-md px-4 py-2 text-sm font-medium text-white bg-violet-700 hover:bg-violet-800 focus:outline-none focus-visible:ring-2 focus-visible:ring-white/75"
            >
               Create New
            </MenuButton>
        </div>

        <transition
            enter-active-class="transition duration-100 ease-out"
            enter-from-class="transform scale-95 opacity-0"
            enter-to-class="transform scale-100 opacity-100"
            leave-active-class="transition duration-75 ease-in"
            leave-from-class="transform scale-100 opacity-100"
            leave-to-class="transform scale-95 opacity-0"
        >
            <MenuItems class="
            absolute right-[-84px] top-[40px] mt-2 w-48 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1
            ring-black/5 focus:outline-none"
            >
                <div class="px-1 py-1">
                    <MenuButton class="w-[100%] text-left hover: hover:bg-violet-500 hover:text-white rounded p-2 text-sm">
                            <span>New Folder</span>
                    </MenuButton>
                </div>
                <div class="px-1 py-1">
                    <MenuButton class="w-[100%] text-left hover: hover:bg-violet-500 hover:text-white rounded p-2 text-sm">
                        <span>Upload Files</span>
                    </MenuButton>
                    <MenuButton class="w-[100%] text-left hover: hover:bg-violet-500 hover:text-white rounded p-2 text-sm">
                        <span>Upload Folder</span>
                    </MenuButton>
                </div>
            </MenuItems>
        </transition>
    </Menu>
</template>

<style scoped>

</style>
