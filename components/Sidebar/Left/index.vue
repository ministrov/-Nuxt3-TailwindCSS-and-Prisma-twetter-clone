<template>
  <div class="flex flex-col h-screen w-min">

    <div class="p-2 my-2 hover:bg-red-300 rounded-full w-min dark:hover:bg-white/20" :class="defaultTransition">
      <NuxtLink to="/">
        <div class="w-8 h-8">
          <LogoTwitter />
        </div>
      </NuxtLink>
    </div>

    <SidebarLeftTab active>
      <template v-slot:icon>
        <HomeIcon/>
      </template>

      <template v-slot:name>
        Home
      </template>
    </SidebarLeftTab>

  </div>
</template>

<script setup>
import {HomeIcon} from '@heroicons/vue/solid';

const {defaultTransition} = useTailwindConfig();

</script>

<style lang="scss" scoped>

</style>