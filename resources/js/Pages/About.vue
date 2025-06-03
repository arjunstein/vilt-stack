<script setup>
import { Head } from '@inertiajs/vue3'
defineProps({
    user: String
})
</script>

<template>
    <Head title="About" />
    <div class="container mx-auto p-4">
        <p>Welcome to the About page, {{ user }}!</p>
    </div>
</template>
