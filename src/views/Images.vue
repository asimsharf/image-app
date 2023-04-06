<script setup>
const copyUrl = async (url) => {
  console.log("copyUrl", url);
  await navigator.clipboard.writeText(url);
};
</script>

<template>
  <VCard class="mx-5 my-2 pa-3">
    <VCardTitle class="text-h5">Image Gallery</VCardTitle>
    <VRow>
      <VCol v-for="n in 200" cols="4" sm="3" md="2" lg="1">
        <VHover v-slot="{ isHovering, props }">
          <VCard :elevation="isHovering ? 12 : 2" v-bind="props">
            <VCard
              :key="n"
              @click="
                copyUrl(`https://picsum.photos/500/300?image=${n * 5 + 10}`)
              "
            >
              <VImg
                :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                aspect-ratio="1"
                cover
              />
              <template v-slot:placeholder>
                <VRow class="fill-height ma-0" align="center" justify="center">
                  <VProgressCircular indeterminate color="grey-lighten-5" />
                </VRow>
              </template>
            </VCard>
          </VCard>
        </VHover>
      </VCol>
    </VRow>
  </VCard>
</template>
