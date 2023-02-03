<script setup>
defineProps({
  desc: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="reasonTile">
    <div class="reasonTile--iconContainer">
      <slot></slot>
    </div>
    <p class="reasonTile--desc">{{ desc }}</p>
  </div>
</template>

<style scoped>
.reasonTile {
  max-width: 21%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.reasonTile--iconContainer {
  width: 50%;
  background-color: #002fe2;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  aspect-ratio: 1;
}
.reasonTile--desc {
  text-align: center;
  margin-top: 20px;
  color: #fff;
}
</style>
