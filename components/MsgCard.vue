<script setup>
const props = defineProps({
    user: 'string',
    msg: 'string',
    created_at: 'string',

})
console.log(props)
</script>

<template>
    <div class="bg-gray-800 my-2 p-2 rounded-lg flex flex-col items-end">
        <div class="pr-2">
            <small class="text-gray-300">@{{ props.user }}</small>
        </div>
        <div class="px-2 pb-4">
            <p class="text-white">{{ props.msg }}</p>
        </div>
        <div>
            <small class="text-white">{{ props.created_at }}</small>
        </div>
    </div>
</template>