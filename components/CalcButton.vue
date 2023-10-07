<template>
<button
    class="
        border border-gray-200
        text-xl
        py-2
        rounded
        shadow
        hover:bg-slate-50
        active:shadow-inner
    "
>{{ title }}</button>
</template>

<script setup lang="ts">
defineProps<{
    title: string
}>()
</script>
