<template>
  <div class="cityList">
    <h3 class="cityList--header">{{ header }}</h3>
    <slot></slot>
    <ul class="cityList-list">
      <li class="cityList-item" v-for="item in list">{{ item }}</li>
    </ul>
  </div>
</template>

<script setup>
defineProps({
  header: {
    type: String,
  },
  list: {
    type: Array,
    required: true,
  },
});
</script>

<style scoped>
.cityList-list {
  column-count: 4;
  list-style: none;
}
.cityList--header {
  text-align: center;
  margin: 30px 0px;
  font-size: 1.7rem;
  line-height: 2rem;
  font-weight: 700;
}
.cityList-item {
  line-height: 110%;
}
.cityList-item:before {
  content: "• ";
  font-size: 27px;
  color: #002de2;
}
</style>
