<template>
    <h1 class="text-center text-neutral-900 font-bold text-3xl mt-6">LAB-VUE-Basic</h1>
    <div class="flex flex-col text-center mt-6">
        <h2 class="text-blue-900 font-bold text-xl">Iteration 1. Create a basic template structure inside a new project
        </h2>
        <p>Creating two components:</p>
        <div class="flex flex-row justify-center content-center align-middle items-center">
            <p>✅ Navbar</p>
            <p>✅ Footer</p>

        </div>
    </div>
    <div class="text-center">
        <h2 class="text-blue-900 font-bold text-xl mt-6">Iteration 2. Display the result of a Javascript operation in a
            component's HTML</h2>
        <p>Mathematical operation: 2+2={{ (2 + 2) }}</p>
        
    </div>
    <div class="text-center">
        <h2 class="text-blue-900 font-bold text-xl mt-6">Iteration 3. Show an element only if a particular property is
            set to true</h2>
        <div class="bg-orange-200 font-bold">
            <p class="show" :class="dinamicBackground">Esto es un texto condicional en MainVue.vue</p>
        </div>

    </div>
    <div class="text-center">
        <h2 class="text-blue-900 font-bold text-xl mt-6 ">Iteration 4. Display a list of elements that are stored inside
            a component</h2>

<!-- Cómo hago para que funcione el V-For??? -->

        <ul>
            <li class="text-dark" v-for="(item, i) in elements" :key="i">
                Name: {{ item.name }} LastName: {{ item.lastName }}
            </li>
        </ul>

    </div>
    <div :class="backgroundColor" class="text-center">
        <h2 class=" font-bold text-xl my-6">Iteration 5. Bonus | Change the background color of an element when pressing
            a button</h2>
    </div>
    <div class="text-center">

<!-- Cómo hago para que funcionen los botones??? -->

        <button class="bg-red-500 text-white font-bold py-2 px-4 hover:bg-red-900"
            @click="changeBackgroundColor('red')">Red</button>
        <button class="bg-blue-500 text-white font-bold py-2 px-4 hover:bg-blue-900"
            @click="changeBackgroundColor('blue')">Blue</button>
        <button class="bg-green-500 text-white font-bold py-2 px-4 hover:bg-green-900"
            @click="changeBackgroundColor('green')">Green</button>
    </div>

</template>

<script setup>
import { ref } from 'vue';

const show = ref('show');
const dinamicBackground = ref('bg-orange-500');
const elements = [
        { name: "Albert", lastName: "Einstein" },
        { name: "Bruno", lastName: "Diaz" },
        { name: "Charles", lastName: "Chaplin" },
        { name: "Donald", lastName: "Duck" }
];

const changeBackgroundColor = color => dinamicBackground.value = `bg-${color}-500`


</script>

<style scoped>
.show {
    display: block;
}

.hidden {
    display: none;
}
</style>