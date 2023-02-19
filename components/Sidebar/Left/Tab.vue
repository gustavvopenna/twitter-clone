<template>
  <nuxt-link to="#"
    class="flex gap-4 items-center p-3 text-black rounded-full hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white"
    :class="defaultTransition"
  >
    <div class="w-6 h-6">
      <slot name="icon">

      </slot>
    </div>
    <div class="hidden xl:block text-xl" :class="textClasses">
      <slot name="name">

      </slot>
    </div>
  </nuxt-link>
</template>

<script setup>
const { defaultTransition } = useTailwind();

const props = defineProps({
  active: {
    type: Boolean,
    default: false
  }
})

const textClasses = computed(() => props.active ? 'font-bold' : 'font-normal')
</script>