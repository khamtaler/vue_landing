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
  flex-wrap: wrap;
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
@media (min-width: 1024px) {
  .reasonTile {
    max-width: 21%;
  }
}
@media (max-width: 1023px) {
  .reasonTile {
    max-width: 90%;
    width: 100%;
    flex-direction: row;
    flex-wrap: nowrap;
    margin: 10px auto;
  }
  .reasonTile--iconContainer {
    width: 100px;
  }
  .reasonTile--desc {
    margin-top: 0px;
    margin-left: 20px;
    width: calc(100vw - 150px);
  }
}
@media (max-width: 500px) {
  .reasonTile {
    max-width: 90%;
    width: 100%;
    flex-direction: column;
    flex-wrap: wrap;
    margin: 10px auto;
  }
  .reasonTile--desc {
    margin-left: 0px;
    width: 100%;
  }
}
</style>
