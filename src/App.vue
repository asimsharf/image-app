<script setup>
import MySideBar from "./components/MySideBar.vue";
</script>

<template>
  <VApp>
    <MySideBar />
    <VMain>
      <VAppBar :elevation="2" rounded height="55">
        <template v-slot:append>
          <VBtn icon="mdi-account-circle" />
          <VBtn icon="mdi-bell" />
          <VBtn icon="mdi-cog" />
        </template>

        <VToolbarTitle class="ml-2" style="font-size: 1.5rem; font-weight: 500">
          <span class="text-primary">I</span>V
          <span class="text-primary">A</span>M
        </VToolbarTitle>
      </VAppBar>

      <router-view />
    </VMain>
  </VApp>
</template>
