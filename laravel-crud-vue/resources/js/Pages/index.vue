<template>
    <div class="container mx-auto pt-5">
        <div class="post_block" v-for="post in posts" :key="post.id">
            <h2>{{ post.title }}</h2>
            <p>{{post.author}}</p>
        </div>
    </div>

</template>

<script setup>
    import { defineProps } from 'vue';

    defineProps({
        posts: Object
    });
</script>