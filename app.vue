<template>
  <div :class="{ 'dark': darkMode }">

    <div class="bg-white dark:bg-dim-900">

      <div class="min-h-full">

        <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5">

          <!-- Left sidebar -->
          <div class="hidden md:block xs-col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <SidebarLeft />
            </div>
          </div>

          <!-- Main content -->
          <main class="col-span-12 bg-red-500 md:col-span-8 xl:col-span-6">
            <h1>Main</h1>
          </main>

          <!-- Right sidebar -->
          <div class="col-span-12 bg-blue-500 md:block xs-col-span-4 xl:col-span-3">
            <div class="sticky top-0">
              <SidebarRight/>
            </div>
          </div>

        </div>

      </div>

    </div>

  </div>
</template>

<script setup>
let darkMode = ref(false);
</script>

<style lang="scss" scoped>

</style>
