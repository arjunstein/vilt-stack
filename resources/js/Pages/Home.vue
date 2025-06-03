<script setup></script>

<template>
    <Head :title="`${$page.component}`" />
    <div class="container mx-auto p-4">
        <h1>{{ $page.props.user }}</h1>
    </div>
</template>
