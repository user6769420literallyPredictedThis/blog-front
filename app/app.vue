<script setup>
import { ref } from 'vue'

const tab = ref(null)

const items = {
  'Home': '/',
  'Cats': '/cats',
  'Kittens': '/kittens',
  'Busya': '/kittens/busya',
  'Bee movie': '/bee'
}
</script>
<template>
  <NuxtLayout>
    <v-app>
        <v-toolbar color="primary">
          <v-app-bar-nav-icon></v-app-bar-nav-icon>

          <v-toolbar-title>Your Dashboard</v-toolbar-title>

          <v-btn icon="mdi-magnify"></v-btn>

          <v-btn icon="mdi-dots-vertical"></v-btn>

          <template v-slot:extension>
            <v-tabs v-model="tab" align-tabs="title">
              <v-tab v-for="(url, name) in items" :key="name" :text="name" :value="name" :to="url"></v-tab>
            </v-tabs>
          </template>
        </v-toolbar>

      <NuxtRouteAnnouncer />
      <NuxtPage />
    </v-app>
  </NuxtLayout>
</template>
