<template>
    <div class="my-2 border border-pink-400 bg-pink-200 p-2">
        <input
            v-model="search"
            type="text"
            placeholder="search..."
            class="border border-gray-400 p-2">
        <button
            class="bg-blue-400 px-6 py-2"
            :disabled="!search"
            @click="go">
            go
        </button>
    </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";

const search = ref(null);

const go = () => {
    console.log(search.value);
}
</script>