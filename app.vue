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
            <CalcButton
                title="AC"
                @click="line = '0'"
            />
            <CalcButton
                title="C"
                @click="cClick()"
            />
        </div>

        <div
            class="
                grid grid-cols-3 gap-2
            "
        >
            <CalcButton
                v-for="i in [1,2,3,4,5,6,7,8,9,0]"
                :title="i"
                :class="{
                    'col-start-2': i === 0,
                }"
                @click="digitClick(i)"
            />
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

function cClick() {
    line.value = line.value.substring(0, line.value.length - 1)
    if(line.value == '') {
        line.value = '0'
    }
}
</script>
