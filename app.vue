<template>
<div class="p-10">
    <h1 class="text-xl mb-10">CalC</h1>
    <div
        class="
            border border-gray-200
            p-5
            space-y-5
        "
    >
        <div
            class="
                border border-gray-200
                p-2
                text-xl text-right
                rounded
            "
        >{{ line }}</div>

        <div
            class="
                grid grid-cols-3 gap-2
            "
        >
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
                @click="line = '0'"
            >AC</button>
        </div>

        <div
            class="
                grid grid-cols-3 gap-2
            "
        >
            <button
                v-for="i in [1,2,3,4,5,6,7,8,9,0]"
                class="
                    border border-gray-200
                    text-xl
                    py-2
                    rounded
                    shadow
                    hover:bg-slate-50
                    active:shadow-inner
                "
                :class="{
                    'col-start-2': i === 0,
                }"
                @click="digitClick(i)"
            >{{ i }}</button>
        </div>
    </div>
</div>
</template>

<script setup lang="ts">
const line = ref('0')

function digitClick(digit: number) {
    if(line.value == '0') {
        line.value = ''
    }
    line.value = line.value + digit.toString()
}
</script>
