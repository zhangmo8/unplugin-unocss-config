<script lang='ts' setup>
console.log(__UNO__)
console.log(import.meta.env.__UNO_THEME__)

console.log(import.meta.env.__UNO__)

const presets = __UNO_CONFIG__.presets?.map((p: any) => p.name)
const transformers = import.meta.env.__UNO__.userConfig.transformers?.map((t: any) => t.name)
</script>

<template>
  <div class="text-white">
    <ul>
      <li v-for="name in presets" :key="name">
        {{ name }}
      </li>
    </ul>
    <ul>
      <li v-for="name in transformers" :key="name">
        {{ name }}
      </li>
    </ul>
  </div>
</template>
