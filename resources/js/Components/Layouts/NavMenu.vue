<template>
    <nav class="text-white font-medium p-6">
        <NavCategory
            v-for="(category, key) in categories"
            :key="key"
            :category="category" />
    </nav>
</template>

<script setup>
import { ref } from '@vue/reactivity';
import NavCategory from './NavCategory'

let categories = ref([
    {
        name: 'Bakery',
        links: [
            { route: '/bread', label: 'bread' },
            { route: '/cake', label: 'cake' },
            { route: '/misc', label: 'misc' },
        ]
    },
    {
        name: 'Beverage',
        links: [
            { route: '/coffee', label: 'coffee' },
            { route: '/tea', label: 'tea' },
            { route: '/soda', label: 'soda' },
        ]
    },
    {
        name: 'Fruit',
        links: [
            { route: '/apple', label: 'apple' },
            { route: '/banana', label: 'banana' },
            { route: '/coconut', label: 'coconut' },
        ]
    }
]);
</script>