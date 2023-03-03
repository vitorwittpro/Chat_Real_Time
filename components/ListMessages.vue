<script setup>

const props = defineProps({
    msgs: Object
})

</script>

<template>
    <div class="h-full w-full flex flex-col justify-end items-end p-5">
        <div class="overflow-y-scroll ">
            <MsgCard v-for="msg in props.msgs" :key="msg.msg_content" :msg="msg" />
        </div>
    </div>
</template>