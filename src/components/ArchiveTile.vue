<script setup>
defineProps({
  year: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="archiveSection--item">
    <h4 class="archiveSection--year">{{ year }}</h4>
    <!-- <img
      class="archiveSection--image"
      :src="`/src/assets/images/${fileName}`"
      :alt="`${altText}`"
    /> -->
    <slot></slot>
  </div>
</template>

<style scoped>
.archiveSection--item {
  width: 23%;
  overflow: hidden;
}
.archiveSection--year {
  text-align: center;
  font-size: 1.2rem;
  font-weight: 500;
}
</style>
