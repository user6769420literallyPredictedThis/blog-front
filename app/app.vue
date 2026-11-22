<script setup lang="ts">
import {
  NavigationMenu,
  NavigationMenuContent,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
  NavigationMenuTrigger,
  navigationMenuTriggerStyle,
} from '@/components/ui/navigation-menu'
</script>

<template>
  <div>
    <NavigationMenu class="p-3">
      <NavigationMenuList>
    
        <NavigationMenuItem>
          <NavigationMenuLink as-child :class="navigationMenuTriggerStyle()">
            <NuxtLink to="/">Home</NuxtLink>
          </NavigationMenuLink>
        </NavigationMenuItem>

        <NavigationMenuItem>
          <NavigationMenuTrigger>Cats</NavigationMenuTrigger>
          <NavigationMenuContent>
            <NavigationMenuLink><NuxtLink to="/cats">Cats</NuxtLink></NavigationMenuLink>
            <NavigationMenuLink><NuxtLink to="/kittens/busya">Busya</NuxtLink></NavigationMenuLink>
            <NavigationMenuLink><NuxtLink to="/kittens">Kittens</NuxtLink></NavigationMenuLink>
          </NavigationMenuContent>
        </NavigationMenuItem>

        <NavigationMenuItem>
          <NavigationMenuLink as-child :class="navigationMenuTriggerStyle()">
            <NuxtLink to="/bee">Bee movie</NuxtLink>
          </NavigationMenuLink>
        </NavigationMenuItem>

      </NavigationMenuList>
    </NavigationMenu>

    <NuxtRouteAnnouncer />
    <NuxtPage />
  </div>
</template>
