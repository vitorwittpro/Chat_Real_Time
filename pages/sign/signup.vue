<script setup>
const user = reactive({
    email: '',
    name: '',
    password: '',
})

async function handleSubmit() {
    await $fetch('http://127.0.0.1:3000/api/users/new', {
        method: 'POST',
        body: {
            "name": user.name,
            "email": user.email,
            "password": user.password,
        }
    })
}
</script>

<template>
    <div>
        <div class="h-screen w-full flex items-center justify-center">
            <div class="bg-gray-300 px-20 py-10 flex flex-col items-center justify-center">
                <h1 class="text-3xl font-bold">Signup</h1>
                <div class="flex flex-col my-5 gap-4" method="POST">
                    <input v-model="user.name" class="bg-transparent bg-white px-2 py-1" type="text" placeholder="name">
                    <input v-model="user.email" class="bg-transparent bg-white px-2 py-1" type="text" placeholder="email">
                    <input v-model="user.password" class="bg-transparent bg-white px-2 py-1" type="text" placeholder="password">
                    <button class="p-5 font-bold bg-white" @click="handleSubmit">Submit</button>
                </div>
            </div>
        </div>
    </div>
</template>