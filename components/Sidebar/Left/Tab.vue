<template>
  <div>
    <NuxtLink to="#" class="flex items-center rounded-full p-3 w-min hover:bg-gray-200" :class="defaultTransition">
      <div class="w-6 h-6 text-dark">
        <slot name="icon"/>
      </div>

      <div class="ml-4 text-xl">
        <slot name="name" :class="textClasses"/>
      </div>
    </NuxtLink>
  </div>
</template>

<script setup>
const {defaultTransition} = useTailwindConfig();

const props = defineProps({
  active: {
    type: Boolean,
    default: false
  }
});

const textClasses = computed(() => props.active ? 'font-semibold' : 'font-normal');
</script>

<style lang="scss" scoped>

</style>