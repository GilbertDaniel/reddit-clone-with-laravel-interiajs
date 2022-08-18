<template>
  <guest-layout>
    <template #header>
      <div class="flex justify-between m-2 p-2">
        <h2 class="font-semibold text-xl text-gray-800 leading-tight">
          r/{{ community.name }}
        </h2>
        <Link
          v-if="$page.props.auth.auth_check"
          :href="route('communities.posts.create', community.slug)"
          class="px-3 py-2 rounded bg-indigo-500 hover:bg-indigo-300 text-white"
          >Create Post</Link
        >
      </div>
    </template>
  </guest-layout>
</template>

<script setup>
import GuestLayout from "@/Layouts/Guest.vue";
import { Link } from "@inertiajs/inertia-vue3";
defineProps({
  community: Object(),
});
</script>
