<template>
    <div class="post_content">
        <h1>{{ post.title }}</h1>
        <p>{{post.author}}</p>
        <div>
          {{ post.content }}
        </div>
    </div>
</template>

<script setup >
    import { defineProps } from 'vue';
    defineProps({
        post: Object
    })
</script>