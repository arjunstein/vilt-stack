<script setup>
const model = defineModel({
    type: null,
    required: true
})

defineProps({
    name: {
        type: String,
        required: true
    },
    type: {
        type: String,
        default: 'text'
    },
    message: String
})
</script>

<template>
    <div>
        <div class="mb-6">
            <label for="{{ name }}">{{ name }}</label>
            <input
                :type="type"
                v-model="model"
                id="{{ name }}"
                :class="{ '!ring-red-500': message }"
            />
            <small class="error" v-if="message">{{ message }}</small>
        </div>
    </div>
</template>
