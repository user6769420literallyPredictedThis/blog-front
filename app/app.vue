<script setup lang="ts">
import {
  NavigationMenu,
  NavigationMenuContent,
  NavigationMenuIndicator,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
  NavigationMenuTrigger,
  NavigationMenuViewport,
} from '@/components/ui/navigation-menu'
</script>

<template>
  <NavigationMenu>
    <NavigationMenuList>
      <NavigationMenuItem>
        <NavigationMenuTrigger>Item One</NavigationMenuTrigger>
        <NavigationMenuContent>
          <NavigationMenuLink>Link</NavigationMenuLink>
        </NavigationMenuContent>
      </NavigationMenuItem>
    </NavigationMenuList>
  </NavigationMenu>
  <div>
    <nav>
      <ul>
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/cats">Cats</nuxt-link></li> <!-- use nuxt-link instead of a href to avoid page reloads -->
        <li><nuxt-link to="/kittens/busya">Busya</nuxt-link></li>
        <li><nuxt-link to="/kittens">Kittens</nuxt-link></li>
        <li><nuxt-link to="/bee">Bee movie</nuxt-link></li>
      </ul>
    </nav>
    <NuxtRouteAnnouncer />
    <NuxtPage />
  </div>
</template>
