<script lang="ts" setup>
const whatsHappeningItems = ref([
    {title: 'SpaceX', count:'10.9k Tweets'},
    {title: '#Coding', count:'10.9k Tweets'},
    {title: 'Art of fun', count:'10.9k Tweets'},
    {title: 'SpaceX', count:'10.9k Tweets'},
]);

const whotoFollowItems = ref([
    {
        name: 'Narand Modi', 
        handle:'@NarandModi',
        image:'https://picsum.photos/200/200'
    },
    {
        name: 'Narand Modi', 
        handle:'@NarandModi',
        image:'https://picsum.photos/200/200'
    },
    {
        name: 'Narand Modi', 
        handle:'@NarandModi',
        image:'https://picsum.photos/200/200'
    },
])

</script>

<template>
    <div class="flex flex-col">
        <!-- Preview card: whats happening -->
        <SideBarRightPreviewCard title="What's happening">
            <SideBarRightPreviewCardItem v-for="whatsHappening in whatsHappeningItems">
                <div>
                    <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>
                    <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
                </div>
            </SideBarRightPreviewCardItem>
        </SideBarRightPreviewCard>
        <!-- Preview card: who to follow -->
        <SideBarRightPreviewCard title="Who to follow">
            <SideBarRightPreviewCardItem v-for="whotoFollow in whotoFollowItems">
                <div class="flex flex-row justify-between items-center p-2">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="whotoFollow.image" :alt="whotoFollow.name"/>
                        <div class="flex flex-col ml-2">
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whotoFollow.name }}</h1>
                            <p class="text-xs text-gray-400">{{ whotoFollow.handle }}</p>
                        </div>
                    </div>
                    <div class="flex h-full ">
                        <button class="px-4 py-2 text-xs font-bold text-white dark:text-black bg-black dark:bg-white rounded-full">Follow</button>
                    </div>
                </div>
            </SideBarRightPreviewCardItem>
        </SideBarRightPreviewCard> 
    </div>
</template>
