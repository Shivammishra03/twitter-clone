<script lang="ts" setup>
const { twitterBorderColor, defaultTransition} = useTailwindConfig();
const props = defineProps({
    title: {
        type: String,
        required: true
    }
});

</script>

<template>
    <div class="bg-gray-50 m-2 border rounded-2xl dark:bg-dim-700" :class="twitterBorderColor">
        <h1 class="p-3 text-xl font-extrabold text-gray-900 border-b dark:text-white">{{ props.title }}</h1>
        <slot></slot>

        <div class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300" :class="defaultTransition">
            Show More
        </div>
    </div>
</template>
