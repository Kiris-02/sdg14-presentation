<script setup lang="ts">
defineProps<{
  dimension: 'Target' | 'Indicator' | 'Measurement' | 'Governance'
  title: string
  color?: string
}>()
</script>

<template>
  <div class="glass-card flex flex-col justify-between h-full border-t-4"
       :class="{
         'border-t-blue-500': dimension === 'Target',
         'border-t-emerald-500': dimension === 'Indicator',
         'border-t-amber-500': dimension === 'Measurement',
         'border-t-purple-500': dimension === 'Governance'
       }">
    <div>
      <div class="flex items-center justify-between mb-2">
        <span class="dim-tag"
              :class="{
                'tag-target': dimension === 'Target',
                'tag-indicator': dimension === 'Indicator',
                'tag-method': dimension === 'Measurement',
                'tag-governance': dimension === 'Governance'
              }">
          Q{{ dimension === 'Target' ? '1: Target' : dimension === 'Indicator' ? '2: Indicator' : dimension === 'Measurement' ? '3: Method' : '4: Governance' }}
        </span>
      </div>
      <h3 class="text-base font-bold text-slate-100 mb-2 leading-snug">{{ title }}</h3>
      <div class="text-xs text-slate-300 space-y-1.5 leading-relaxed">
        <slot />
      </div>
    </div>
  </div>
</template>
