<template>
    <authenticated-layout>
        <div class="container">
            <table class="table-auto">
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Nama</th>
                        <th>Alamat</th>
                        <th>Create</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="user in users" :key="user.id">
                        <td>{{ user.id }}</td>
                        <td>{{ user.name }}</td>
                        <td>{{ user.email }}</td>
                        <td class="cursor-pointer">Create</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </authenticated-layout>
</template>

<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';

defineProps({
    users: Array,
});
</script>

<style lang="postcss" scoped>
th,
td {
    @apply border-b p-2;
}
</style>
