<script lang="ts" setup>
const { defaultTransition } = useTailwindConfig();
import { HomeIcon } from  "@heroicons/vue/solid";
import { SearchIcon,BookmarkIcon,BellIcon,DotsCircleHorizontalIcon,UserIcon, DocumentTextIcon } from  "@heroicons/vue/outline";

</script>

  
<template>
    <div class="flex flex-col h-screen">
        <div class="p-2 my-2 hover:bg-gray-200 rounded-full w-min dark:hover:bg-white/20" :class="defaultTransition">
            <NuxtLink to="/">
                <div class="w-8 h-8">
                    <LogoTwitter></LogoTwitter>
                </div>
            </NuxtLink>
        </div>
        <div class="mt-2 space-y-3">
            <SideBarLeftTab active>
                <template v-slot:icon>
                    <HomeIcon/>
                </template>
                <template v-slot:name>
                    Home
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <SearchIcon/>
                </template>
                <template v-slot:name>
                    Explore
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <BellIcon/>
                </template>
                <template v-slot:name>
                   Notifications
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                    </svg>
                </template>
                <template v-slot:name>
                    Messages
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <BookmarkIcon/>
                </template>
                <template v-slot:name>
                   Bookmarks
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <DocumentTextIcon/>
                </template>
                <template v-slot:name>
                    Lists
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <UserIcon/>
                </template>
                <template v-slot:name>
                    Profile
                </template>
            </SideBarLeftTab>
            <SideBarLeftTab>
                <template v-slot:icon>
                    <DotsCircleHorizontalIcon/>
                </template>
                <template v-slot:name>
                    More
                </template>
            </SideBarLeftTab>

        </div>
    </div>
</template>