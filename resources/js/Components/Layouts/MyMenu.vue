<template>
    <nav class="my-2 border border-purple-400 bg-purple-200 p-2">
        <p>This is menu</p>
        <ul>
            <li v-for="item in menuItems" :key="item">
                <button @click="$emit('menuClicked', item)">{{ item }}</button>
            </li>
        </ul>
    </nav>
</template>

<script setup>
defineProps({
    menuItems: { type: Array, default: [] }
});

defineEmits(['menuClicked']);
</script>