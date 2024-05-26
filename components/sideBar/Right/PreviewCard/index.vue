<script lang="ts" setup>
const {twitterBorderColor} = useTailwindConfig();
const props = defineProps({
    title: {
        type: String,
        required: true
    }
});

</script>

<template>
    <div class="bg-gray-50 m-2 border" :class="twitterBorderColor">
        <h1>{{ props.title }}</h1>
    </div>
</template>
