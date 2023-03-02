<script setup>
const message = reactive({
    user_id: '18',
    msg_content: '',
    created_at: 'NOW()',
})

async function sendMessage() {
    await $fetch('http://127.0.0.1:3000/api/messages/new',
        {
            method: 'POST',
            body: {
                "created_at": "NOW()",
                "user_id": message.user_id,
                "msg_content": message.msg_content
            },
        })

    console.log(message)
}

</script>

<template>
    <div class="bg-gray-200 w-full p-10">
        <div class="border h-full flex flex-col">
            <div class="h-full w-full flex flex-col justify-end items-end p-5">
                <div class="bg-gray-800 p-2 rounded-lg flex flex-col items-end">
                    <div class="pr-2">
                        <small class="text-gray-300">@Orochi</small>
                    </div>
                    <div class="px-2 pb-4">
                        <p class="text-white">Sending a message</p>
                    </div>
                    <div>
                        <small class="text-white">14:00</small>
                    </div>
                </div>
            </div>
            <div class="relative w-full">
                <input v-model="message.msg_content" class="w-full p-5 rounded-full text-xl focus:outline-none" type="text" placeholder="Type your message">
                <div class="absolute bg-transparent border-none top-0 right-0 flex items-center border h-full mr-1">
                    <button @click="sendMessage" class="bg-gray-900 rounded-full p-3 flex">
                        <img class="w-[35px] h-[35px]" src="~~/assets/send.png" alt="send">
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>