<template>
    <div>
        <header class="bg-indigo-800 text-white p-4">
            <nav class="flex justify-between items-center max-w-7xl mx-auto">
                <div class="space-x-6">
                    <a href="/">Home</a>
                    <a href="/about">About</a>
                </div>
            </nav>
        </header>
        <main class="p-4">
            <slot />
        </main>
    </div>
</template>
