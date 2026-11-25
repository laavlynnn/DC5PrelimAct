<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, usePage } from '@inertiajs/vue3';

const user = usePage().props.auth.user;

const hours = new Date().getHours();

let greeting = '';

if (hours < 12) {
    greeting = 'Good morning';
} else if (hours < 18) {
    greeting = 'Good afternoon';
} else {
    greeting = 'Good evening';
}
</script>

<template>
    <Head title="Catalogs" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="text-xl font-semibold leading-tight text-gray-800">
                Catalogs
            </h2>
        </template>

        <div class="py-12">
            <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
                <div class="overflow-hidden bg-white shadow-sm sm:rounded-lg">
                    <div class="p-6 text-gray-900">
                        <h1 class="text-lg font-semibold">
                            {{ greeting }}, {{ user.name }}!
                        </h1>
                    </div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>