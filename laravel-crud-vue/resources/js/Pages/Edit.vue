<template>
    <div class="post__create">
        <form @submit.prevent="form.put(`/post/update/${post.id}`)">
            <div>
                <label>Title</label>
                <input type="text" v-model="form.title"/>
            </div>
            <div>
                <label>Author</label>
                <input type="text" v-model="form.author"/>
            </div>
            <div>
                <label>Content</label>
                <textarea v-model="form.content"></textarea>
            </div>
            <div>
                <input type="submit" value="Update post">
            </div>
        </form>
    </div>
</template>

<script setup>
    import { useForm } from '@inertiajs/vue3';
    import { defineProps } from 'vue';

    let props = defineProps({
        post: Object
    })

    const form = useForm({
        title: props.post.title,
        author: props.post.author,
        content: props.post.content
    })
</script>