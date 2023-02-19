<template>
  <div :class="{ dark: isDarkMode }">
    <div class="min-h-full bg-white dark:bg-dim-900">
      <div class="grid grid-cols-12 mx-auto sm:px-6 lg:px-8 lg:max-w-7xl lg:gap-4">
        <aside class="hidden md:block xs:col-span-1 xl:col-span-2">
          <div class="sticky top-0">
            <SidebarLeft />
          </div>
        </aside>
        <main class="col-span-12 md:col-span-8 xl:col-span-6 bg-red-500">
          Hello
        </main>
        <aside class="hidden md:block xl:col-span-4 md:col-span-3 bg-blue-500">
          <h2>Right sidebar</h2>
        </aside>
      </div>
    </div>
  </div>
</template>

<script setup>
const isDarkMode = ref(false);
</script>
