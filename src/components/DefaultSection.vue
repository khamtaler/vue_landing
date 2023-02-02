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
    <h3 class="section--header">{{ header }}</h3>
    <hr class="section---headerUnderline" />
    <slot></slot>
  </section>
</template>

<style scoped>
.section--header {
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
