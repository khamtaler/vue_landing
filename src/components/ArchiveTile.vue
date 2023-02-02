<script setup>
defineProps({
  year: {
    type: String,
    required: true,
  },
  fileName: {
    type: String,
    required: true,
  },
  altText: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="archiveSection--item">
    <h4 class="archiveSection--year">{{ year }}</h4>
    <img
      class="archiveSection--image"
      :src="`/src/assets/images/${fileName}`"
      :alt="`${altText}`"
    />
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

.archiveSection--item:hover {
  overflow: visible;
}
.archiveSection--image {
  width: 100%;
  height: 300px;
}
.archiveSection--item:hover .archiveSection--image {
  scale: 1.5;
  z-index: 2;
}
</style>
