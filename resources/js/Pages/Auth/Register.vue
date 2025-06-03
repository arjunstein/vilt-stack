<script setup>
import { useForm } from '@inertiajs/vue3'

const form = useForm({
    name: null,
    email: null,
    password: null,
    password_confirmation: null
})

const submit = () => {
    form.post(route('register'), {
        onError: () => form.reset('password', 'password_confirmation')
    })
}
</script>

<template>
    <Head title="Register" />

    <h1 class="title">Register a new account</h1>
    <div class="w-2/4 mx-auto">
        <form @submit.prevent="submit">
            <div class="mb-6">
                <label for="name">Name</label>
                <input type="text" v-model="form.name" id="name" />
                <small class="text-red-500">{{ form.errors.name }}</small>
            </div>
            <div class="mb-6">
                <label for="email">Email</label>
                <input type="text" v-model="form.email" id="email" />
                <small class="text-red-500">{{ form.errors.email }}</small>
            </div>

            <div class="mb-6">
                <label for="password">Password</label>
                <input type="password" v-model="form.password" id="password" />
                <small class="text-red-500">{{ form.errors.password }}</small>
            </div>

            <div class="mb-6">
                <label for="password_confirm">Confirm Password</label>
                <input
                    type="password"
                    v-model="form.password_confirmation"
                    id="password_confirm"
                />
            </div>

            <div>
                <p class="text-slate-600 mb-2">
                    Already a user? <a href="#" class="text-link">Login</a>
                </p>
                <button class="primary-btn">Register</button>
            </div>
        </form>
    </div>
</template>
