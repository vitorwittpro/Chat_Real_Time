<script setup>
const url = 'http://127.0.0.1:3000/api/users'

const users = useFetch(url).then((response) => response.data)
console.log(users)
</script>

<template>
    <div class="w-[600px] h-screen p-5  bg-[rgb(0,0,0)] ">
        <h1 class="font-bold text-3xl text-white">Consuming API</h1>
        <div class="h-full mt-10 p-2">
            <ul class="flex flex-col gap-3">
                <li class="rounded-lg px-2 py-4 bg-[#231828]">
                    <div class="mb-2 ml-2">
                        <h2 class="text-white font-bold">channel #1</h2>
                    </div>
                    <div class="pl-5 pr-2 flex flex-col gap-2">
                        <div class="w-full">
                            <div class="flex items-center gap-3 p-2 rounded-lg  bg-[#C1B5C7]">
                                <div class="bg-[rgb(16,16,16)] w-[40px] h-[40px] rounded-full flex items-center">
                                    <h1 class="w-full text-center font-bold text-xl text-white">M</h1>
                                </div>
                                <h2 class="font-bold">Mitinho</h2>
                            </div>
                        </div>
                        <div class="w-full">
                            <div class="flex items-center gap-3 p-2 rounded-lg  bg-[#C1B5C7]">
                                <div class="bg-[rgb(16,16,16)] w-[40px] h-[40px] rounded-full flex items-center">
                                    <h1 class="w-full text-center font-bold text-xl text-white">P</h1>
                                </div>
                                <h2 class="font-bold">Pisca</h2>
                            </div>
                        </div>
                        <div class="w-full">
                            <div class="flex items-center gap-3 p-2 rounded-lg  bg-[#C1B5C7]">
                                <div class="bg-[rgb(16,16,16)] w-[40px] h-[40px] rounded-full flex items-center">
                                    <h1 class="w-full text-center font-bold text-xl text-white">O</h1>
                                </div>
                                <h2 class="font-bold">Orochinho</h2>
                            </div>
                        </div>
                    </div>
                </li>
                <li class="rounded-lg p-4 bg-[#231828]">
                    <div class="">
                        <h2 class="text-white font-bold">channel #2</h2>
                    </div>
                </li>
                <li class="rounded-lg p-4 bg-[#231828]">
                    <div class="">
                        <h2 class="text-white font-bold">channel #2</h2>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>