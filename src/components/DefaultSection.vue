<script setup>
defineProps({
  header: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <section class="section section---vertical">
    <div class="section--headerContainer">
      <h3 class="section--header">{{ header }}</h3>
      <hr class="section---headerUnderline" />
    </div>
    <slot></slot>
  </section>
</template>

<style scoped>
.section--headerContainer {
  margin: auto;
  width: 100%;
}

.section--header {
  width: 100%;
  font-size: 1.7rem;
  line-height: 2rem;
  font-weight: 700;
  text-align: center;
}
.section---headerUnderline {
  width: 50px;
  margin: auto;
  height: 5px;
  background: #e7e7e7;
  color: #e7e7e7;
  border: unset;
  margin-top: 10px;
  margin-bottom: 30px;
}
</style>
