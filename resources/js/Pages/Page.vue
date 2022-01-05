<template>
    <!-- main container -->
    <main class="bg-green-200 p-4">
        <h1>Page name</h1>

        <p>menu clicked: {{ selectedMenu }}</p>

        <!-- menu -->
        <MyMenu
            :menuItems="menuItems"
            @menuClicked="(item) => selectedMenu = item"
            />

        <!-- search -->
        <SearchForm />

        <!-- page content -->
        <div class="my-2 border-gray-400 bg-gray-200 p-2">
            <h2>this is content</h2>
            <article>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Assumenda voluptatum illum deleniti cupiditate voluptas delectus sit, earum nihil labore nam voluptatem beatae corrupti inventore neque dolor officia quod quos autem!
            </article>
        </div>

        <!-- contact form -->
        <ContactForm />
    </main>
</template>

<script setup>
import MyMenu from '@/Components/Layouts/MyMenu'
import SearchForm from '@/Components/Layouts/SearchForm'
import ContactForm from '@/Components/Layouts/ContactForm'
import { ref } from '@vue/reactivity';

defineProps({
    menuItems: { type: Array, default: [] }
});

const selectedMenu = ref('');
</script>