<script setup>
const list_abouts = [
  {
    title: "About",
    ocupation: "Software Developer",
    avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  },
  {
    title: "Contact",
    ocupation: "Software Developer",
    avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  },
  {
    title: "Help",
    ocupation: "Software Developer",
    avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  },
];
</script>

<template>
  <VCard class="mx-5 my-2 pa-3">
    <VCardTitle class="text-h5">About</VCardTitle>
    <VCol>
      <VList lines="three">
        <VListItem
          v-for="about in list_abouts"
          :key="about.title"
          :title="about.title"
          :subtitle="about.ocupation"
          :prepend-avatar="about.avatar"
          class="ma-5"
          variant="outlined"
          >{{ about.description }}</VListItem
        >
      </VList>
    </VCol>
  </VCard>
</template>
