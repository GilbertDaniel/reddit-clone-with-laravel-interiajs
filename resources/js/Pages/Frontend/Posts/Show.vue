<template>
    <guest-layout>
        <section class="flex flex-col md:flex-row m-2 p-2">
            <div class="w-full md:w-8/12">
                <h1>{{post.title}}</h1>
                Post Details Goes Here!
            </div>
            <div class="2-4/12 p-4">
                <div class="m-2 p-2 bg-slate-500 text-white">
                    <h2>Latests Communitites</h2>
                </div>
            </div>
        </section>
    </guest-layout>
</template>

<script setup>
import GuestLayout from "@/Layouts/Guest.vue";
import { Link } from "@inertiajs/inertia-vue3";

const props = defineProps({
    community: Object,
    post: Object,
});
</script>
