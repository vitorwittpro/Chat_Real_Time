<script setup>

const newMsg = ref('')

const typeMsg = reactive({
    created_at: 'NOW()',
    user_id: '18',
    msg: newMsg
})

const { data } = await useFetch('http://127.0.0.1:3000/api/messages')
const msgs = toRaw(data.value)


async function sendMessage() {

    await $fetch('http://127.0.0.1:3000/api/messages/new',
        {
            method: 'POST',
            body: {
                "created_at": typeMsg.created_at,
                "user_id": typeMsg.user_id,
                "msg_content": typeMsg.msg
            },
        })
    console.log(typeMsg)
}

</script>

<template>
    <div class="bg-gray-200 w-full p-10">
        <div class="border h-full flex flex-col">
            <ListMessages :msgs="msgs" />
            <div class="relative w-full">
                <input v-model="newMsg" class="w-full p-5 rounded-full text-xl focus:outline-none" type="text" placeholder="Type your message">
                <div class="absolute bg-transparent border-none top-0 right-0 flex items-center border h-full mr-1">
                    <button @click="sendMessage" class="bg-gray-900 rounded-full p-3 flex">
                        <img class="w-[35px] h-[35px]" src="~~/assets/send.png" alt="send">
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>