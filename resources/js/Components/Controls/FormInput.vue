<template>
    <div class="mt-1">
        <div>
            <input
                :value="modelValue"
                @input="$emit('update:modelValue', $event.target.value)"
                :type="inputType"
                :placeholder="inputPlaceholder"
                class="border border-gray-400 p-2">
        </div>
        <!-- show error -->
        <small
            class="text-sm text-red-400"
            v-if="error"
        >
            {{ error }}
        </small>
    </div>
</template>

<script setup>

defineProps({
    modelValue: { type: String, default: '' },
    inputType: { type: String, default: 'text' },
    inputPlaceholder: { type: String, default: '' },
    error: { type: String, default: '' },
});

defineEmits(['update:modelValue'])

</script>