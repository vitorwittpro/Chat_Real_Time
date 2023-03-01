<script setup>
useHead({ title: 'Consuming API' })
</script>

<template>
    <div class="w-full my-10 mx-5 flex items-end">
        <div></div>
        <div class="w-full flex flex-row items-center">
            <input class="w-full py-7 px-7 text-xl rounded-full" type="text" placeholder="Type your message" />
            <button class="absolute right-8 bg-sky-900 py-3 px-3 rounded-full">
                <img src="@/assets/send.png" alt="asd">
            </button>
        </div>
    </div>
</template>