<template>
    <form class="my-2 border-indigo-400 bg-indigo-200 p-2">
        <h2>contact us</h2>
        <FormInput
            v-model="form.message"
            inputPlaceholder="message"
            :error="form.errors.message" />

        <FormInput
            v-model="form.email"
            inputType="email"
            inputPlaceholder="email"
            :error="form.errors.email" />

        <button class="bg-blue-400 mt-1 px-6 py-2">submit</button>
    </form>
</template>

<script setup>
import FormInput from '@/Components/Controls/FormInput'
import { useForm } from '@inertiajs/inertia-vue3'
import { onMounted } from '@vue/runtime-core';

const form = useForm({
    message: '',
    email: '',
});

onMounted(() => {
    form.errors.message = 'too long';
});
</script>