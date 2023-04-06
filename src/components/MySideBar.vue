<script setup>
</script>

<template>
  <VNavigationDrawer expand-on-hover rail>
    <VList>
      <VListItem
        prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
        title="Asim Sharfeldin"
        subtitle="asimsharf@gmailcom"
      >
      </VListItem>
      <VDivider />
    </VList>

    <VList density="compact" nav>
      <VListItem
        to="/"
        prepend-icon="mdi-home"
        title="Dashboard"
        value="dashboard"
      >
      </VListItem>
      <VListItem
        to="/images"
        prepend-icon="mdi-image"
        title="Image"
        value="image"
      >
      </VListItem>
      <VListItem
        to="/about"
        prepend-icon="mdi-information"
        title="About"
        value="about"
      >
      </VListItem>
    </VList>
  </VNavigationDrawer>
</template>
