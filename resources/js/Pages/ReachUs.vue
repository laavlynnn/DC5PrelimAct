<script setup>
import { Head, Link } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Reach Us" />

    <div class="min-h-screen bg-gray-100">
        <nav class="border-b border-gray-100 bg-white">
            <div class="mx-auto flex h-16 max-w-7xl items-center justify-between px-4 sm:px-6 lg:px-8">
                <Link href="/" class="font-semibold text-gray-800">Home</Link>
                <div class="space-x-4 text-sm text-gray-600">
                    <Link :href="route('catalog')" class="hover:text-gray-900">Catalogs</Link>
                    <Link :href="route('login')" class="hover:text-gray-900">Log in</Link>
                </div>
            </div>
        </nav>

        <main class="mx-auto max-w-3xl px-4 py-12">
            <div class="rounded-lg bg-white p-8 shadow-sm">
                <h1 class="text-2xl font-semibold text-gray-800">Reach Us</h1>
                <p class="mt-4 text-gray-600">
                    Have questions? Get in touch with us.
                </p>
                <ul class="mt-4 space-y-2 text-gray-700">
                    <li>Email: hello@example.com</li>
                    <li>Phone: +63 900 000 0000</li>
                    <li>Address: Clarin, Bohol, Philippines</li>
                </ul>
            </div>
        </main>
    </div>
</template>