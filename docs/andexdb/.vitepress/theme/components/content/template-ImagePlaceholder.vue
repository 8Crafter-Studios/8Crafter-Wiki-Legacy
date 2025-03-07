<script setup lang="ts">
const props = defineProps<{
  size?: number
}>();
</script>
<template>
  <image src="/assets/images/icons/missing_pack_icon.png" :width="props.size ?? 64" :height="props.size ?? 64" />
</template>
