<template>
    <div class="post__create">
        <form @submit.prevent="form.post('/post')">
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
                <input type="submit" value="Create new post">
            </div>
        </form>
    </div>
</template>

<script setup>
    import { useForm } from '@inertiajs/vue3';

    const form = useForm({
        title: '',
        author: '',
        content: ''
    })
</script>