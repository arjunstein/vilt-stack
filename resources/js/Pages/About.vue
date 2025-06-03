<template>
    <div>
        <h1>About Us</h1>
        <p>Welcome to the About page, {{ user }}!</p>
    </div>
</template>

<script setup>
defineProps({
    user: String
})
</script>
