<script setup>

const props = defineProps({
    user: String
})

const firstLetter = (str) => {
    return str[0].toUpperCase()
}

</script>


<template>
    <div class="w-full">
        <div class="flex items-center gap-3 p-2 rounded-lg  bg-[#C1B5C7]">
            <div class="bg-[rgb(16,16,16)] w-[40px] h-[40px] rounded-full flex items-center">
                <h1 class="w-full text-center font-bold text-xl text-white">{{ firstLetter(user) }}</h1>
            </div>
            <h2 class="font-bold">{{ user }}</h2>
        </div>
    </div>
</template>