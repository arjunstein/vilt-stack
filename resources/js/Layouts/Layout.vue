<script setup></script>

<template>
    <div>
        <header class="bg-gray-800 text-white p-4">
            <nav class="flex justify-between items-center max-w-7xl mx-auto">
                <div class="space-x-6">
                    <Link :href="route('home')" class="hover:text-gray-300"
                        >Home</Link
                    >
                    <Link :href="route('about')" class="hover:text-gray-300"
                        >About</Link
                    >
                </div>
            </nav>
        </header>
        <main class="p-4">
            <slot />
        </main>
    </div>
</template>
