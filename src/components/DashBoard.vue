<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";
const router = useRouter();

const users = () => {
  console.log("users");
  router.push({ name: "Users" });
};

const images = () => {
  console.log("images");
  router.push({ name: "Image" });
};

const folders = () => {
  console.log("folders");
  router.push({ name: "Folders" });
};

const groups = () => {
  console.log("groups");
  router.push({ name: "Groups" });
};

const desserts = [
  {
    name: "Shawky Mohamed Shawky",
    age: 34,
    phone: "+966 5674 34 123",
    country: "USA",
    city: "New York",
  },
  {
    name: "Omer Ahmed Amasib",
    age: 32,
    phone: "+966 5674 34 123",
    country: "USA",
    city: "Los Angeles",
  },
  {
    name: "Mohamed ali ahmed ibrahim",
    age: 53,
    phone: "+966 5674 34 123",
    country: "USA",
    city: "Los Angeles",
  }
];
</script>

<template>
  <VCard class="mx-5 my-2 pa-3">
    <VCardTitle class="text-h5">
      <VIcon class="mr-2" size="30" color="primary">mdi-home</VIcon>
      DASHBOARD
    </VCardTitle>
    <VDivider />

    <VRow>
      <VHover v-slot="{ isHovering, props }">
        <VSheet
          class="ma-auto mt-10 my-10 rounded-shaped"
          :elevation="isHovering ? 12 : 3"
          @click="users"
          v-bind="props"
          height="150"
          width="320"
        >
          <VCardTitle class="text-h5" align="center">
            <VIcon class="mr-2" size="30" color="primary">mdi-account</VIcon>
            USERS
          </VCardTitle>
          <VDivider />
        </VSheet>
      </VHover>

      <VHover v-slot="{ isHovering, props }">
        <VSheet
          class="ma-auto mt-10 my-10 rounded-shaped"
          :elevation="isHovering ? 12 : 3"
          @click="images"
          v-bind="props"
          height="150"
          width="330"
        >
          <VCardTitle class="text-h5" align="center">
            <VIcon class="mr-2" size="30" color="primary">mdi-image</VIcon>
            IMAGES
          </VCardTitle>
          <VDivider />
        </VSheet>
      </VHover>

      <VHover v-slot="{ isHovering, props }">
        <VSheet
          class="ma-auto mt-10 my-10 rounded-shaped"
          :elevation="isHovering ? 12 : 3"
          @click="folders"
          v-bind="props"
          height="150"
          width="330"
        >
          <VCardTitle class="text-h5" align="center">
            <VIcon class="mr-2" size="30" color="primary">mdi-folder</VIcon>
            FOLDERS
          </VCardTitle>
          <VDivider />
        </VSheet>
      </VHover>

      <VHover v-slot="{ isHovering, props }">
        <VSheet
          class="ma-auto mt-10 my-10 rounded-shaped"
          :elevation="isHovering ? 12 : 3"
          @click="groups"
          v-bind="props"
          height="150"
          width="330"
        >
          <VCardTitle class="text-h5" align="center">
            <VIcon class="mr-2" size="30" color="primary"
              >mdi-account-group</VIcon
            >
            GROUPS
          </VCardTitle>
          <VDivider />
        </VSheet>
      </VHover>
    </VRow>
  </VCard>
  <VTable>
    <thead>
      <tr>
        <th class="text-left">Name</th>
        <th class="text-left">Age</th>
        <th class="text-left">Phone</th>
        <th class="text-left">Country</th>
        <th class="text-left">City</th>
        <th class="text-end">Action</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="item in desserts" :key="item.age">
        <td>{{ item.name }}</td>
        <td>{{ item.age }}</td>
        <td>{{ item.phone }}</td>
        <td>{{ item.country }}</td>
        <td>{{ item.city }}</td>
        <td class="text-end">
          <VIcon class="mr-1" size="20" color="success">mdi-pencil</VIcon>
          <VIcon class="mr-1" size="20" color="error">mdi-delete</VIcon>
        </td>
      </tr>
    </tbody>
  </VTable>
</template>
