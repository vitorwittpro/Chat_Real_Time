<script setup>

const props = defineProps({
    msg: Object
})

console.log(props.msg.user_id)

</script>

<template>
    <div class="bg-gray-800 my-2 p-2 rounded-lg flex flex-col items-end">
        <div class="pr-2 w-full flex items-start">
            <small class="text-gray-300 text-xs">@{{ msg.user_id }}</small>
        </div>
        <div class="px-2 pb-4">
            <p class="text-white">{{ msg.msg_content }}</p>
        </div>
        <div>
            <small class="text-white">{{ msg.created_at }}</small>
        </div>
    </div>
</template>