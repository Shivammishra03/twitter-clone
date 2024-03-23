<script setup>
const darkMode = ref();
</script>
<template>
  <div :class="{'dark':darkMode}">
    <div class="min-h-full">
      <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5">
        <!-- left Sidebar -->
        <div class="hidden bg-red-500 md:block xs-col-span-1 xl:col-span-2">
          <div class="sticky top-0">
            shivam
          </div>
        </div>
        <!-- Main  content and body of the page -->
        <!-- right  side bar -->
      </div>
    </div>
  </div>
</template>
