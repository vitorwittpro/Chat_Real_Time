<script setup>

const props = defineProps({
    msg: 'object'
})

console.log(props.msg.user_id)

</script>

<template>
    <div class="h-full w-full flex flex-col justify-end items-end p-5">
        <MsgCard :user="props.msg.user_id" :msg="props.msg.msg_content" :created_at="props.msg.created_at" />
    </div>
</template>