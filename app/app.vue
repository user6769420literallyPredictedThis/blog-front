<template>
  <div>
    <nav>
      <ul>
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/cats">Cats</nuxt-link></li> <!-- use nuxt-link instead of a href to avoid page reloads -->
        <li><nuxt-link to="/kittens/busya">Busya</nuxt-link></li>
        <li><nuxt-link to="/kittens">Kittens</nuxt-link></li>
      </ul>
    </nav>
    <NuxtRouteAnnouncer />
    <NuxtPage />
  </div>
</template>
