<template>
    <div class="bg-green-200 p-4">
        <QuillEditor v-model:content="form.delta" />
    </div>
    <div class="bg-pink-200 p-4">
        {{ form }}
    </div>
    <div class="bg-blue-200 p-4">
        <button
            @click="insertDelta"
            class="border border-blue-400 py-2 px-4 text-blue-400">Insert</button>
    </div>
</template>

<script setup>
import { computed, reactive } from '@vue/reactivity';
import { watch } from '@vue/runtime-core';
import { QuillEditor } from '@vueup/vue-quill'
import '@vueup/vue-quill/dist/vue-quill.snow.css';

const form = reactive({
    // delta: {ops: []}
    delta: { "ops": [ { "insert": "hello\nworld\n" } ] }
});

const insertDelta = () => {
    let temp = form.delta;
    form.delta = {};
    setTimeout(() => form.delta = temp, 2000);
};
</script>