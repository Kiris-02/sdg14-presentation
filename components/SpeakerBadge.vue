<script setup lang="ts">
defineProps<{
  speaker: string | number
  time: string
  role?: string
}>()
</script>

<template>
  <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-cyan-950/60 border border-cyan-500/40 text-cyan-300 text-xs font-semibold backdrop-blur shadow-sm">
    <span class="w-2 h-2 rounded-full bg-cyan-400 animate-pulse"></span>
    <span>Speaker {{ speaker }}</span>
    <span class="text-cyan-500">•</span>
    <span class="text-slate-300">{{ time }}</span>
    <span v-if="role" class="text-cyan-500">•</span>
    <span v-if="role" class="text-emerald-400 font-medium">{{ role }}</span>
  </div>
</template>
