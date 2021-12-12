<template>
    <div>
        <button @click="showItems = !showItems">
            <h3 class="text-lg mt-4">{{ category.name }}</h3>
        </button>
        <transition name="slide-fade">
            <ul class="ml-4 mt-2 space-y-2" v-if="showItems">
                <li v-for="(link, key) in category.links" :key="key">
                    <a :href="link.route">{{ link.label[0].toUpperCase() + link.label.slice(1) }}</a>
                </li>
            </ul>
        </transition>
    </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";

defineProps({
    category: { type: Object, required: true }
});

let showItems = ref(false);

</script>