<script setup>
import { Head, Link } from "@inertiajs/vue3";
import TwitterLayout from "@/Layouts/TwitterLayout.vue";
import Tweet from "@/Components/Tweet.vue";

defineProps({ tweets: Array })
</script>

<template>
    <Head title="Welcome" />
    <TwitterLayout>
      <div class="text-white">
        <div class="flex" v-for="tweet in tweets" :key="tweet">
          <Tweet :tweet="tweet" />
        </div>
        <div class="border-b-slate-800 mt-2 border-b"></div>
      </div>
    </TwitterLayout>
</template>
