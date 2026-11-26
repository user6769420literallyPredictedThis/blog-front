<script setup lang="ts">
import type { BlogPostProps } from '@nuxt/ui'
import { faker } from '@faker-js/faker';

const posts = ref<BlogPostProps[]>([
    {
        title: 'Nuxt Icon v1',
        description: 'Discover Nuxt Icon v1!',
        image: 'https://nuxt.com/assets/blog/nuxt-icon/cover.png',
        date: '2024-11-25',
    },
    {
        title: 'Nuxt 3.14',
        description: 'Nuxt 3.14 is out!',
        image: 'https://nuxt.com/assets/blog/v3.14.png',
        date: '2024-11-04',
    },
    {
        title: 'Nuxt 3.13',
        description: 'Nuxt 3.13 is out!',
        image: 'https://nuxt.com/assets/blog/v3.13.png',
        date: '2024-08-22',
    },
]);
for (let i = 0; i < 20; i++) {
    posts.value.push({
        title: faker.lorem.sentence(),
        description: faker.lorem.paragraph(),
        image: faker.image.url({ width: 1280, height: 720 }),
        date: faker.date.past()
    })
};
</script>

<template>
    <UBlogPosts
        class="lg:grid-cols-4"
        :posts="posts"
    />
</template>