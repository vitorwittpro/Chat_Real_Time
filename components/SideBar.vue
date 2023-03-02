<script setup>
const url = 'http://127.0.0.1:3000/api/users'

const usersData = await useFetch(url).then((response) => response.data)

const users = usersData.value;
</script>

<template>
    <div class="w-[500px] h-full p-5  bg-[rgb(0,0,0)] ">
        <h1 class="font-bold text-3xl text-white">Consuming API</h1>
        <div class="h-full mt-10 p-2">
            <ul class="flex flex-col gap-3">
                <li class="rounded-lg px-2 py-4 bg-gray-800">
                    <div class="mb-2 ml-2">
                        <h2 class="text-white font-bold">channel #1</h2>
                    </div>
                    <div class="pl-5 pr-2 flex flex-col gap-2">
                        <UserCard v-for="user in users" :key="user.name" :user="user.name" />
                    </div>
                </li>

            </ul>
        </div>
    </div>
</template>