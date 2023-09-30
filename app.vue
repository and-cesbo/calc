<template>
<div class="p-10">
    <h1 class="text-xl mb-10">CalC</h1>
    <div class="border border-gray-200 p-5">
        <div
            class="
                border border-gray-200
                mb-5 p-2
                text-xl text-right

            "
        >тут будут цифры</div>

        <div
            class="
                border border-gray-200 p-2
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
                "
            >{{ i }}</button>
        </div>
    </div>
</div>
</template>
