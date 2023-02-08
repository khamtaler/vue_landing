<template>
  <div class="cityList">
    <h3 class="cityList--header">{{ header }}</h3>
    <slot></slot>
    <ul class="cityList--list">
      <li class="cityList--item" v-for="(item, index) in list" :key="index">{{ item }}</li>
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
.cityList--list {
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
.cityList--item {
  line-height: 110%;
}
.cityList--item:before {
  content: "• ";

  color: #002de2;
}
@media (max-width: 1200px) {
  .cityList--list {
    text-align: start;
  }
}

@media (min-width: 901px) {
  .cityList--item:before {
    font-size: 27px;
  }
}
@media (max-width: 900px) {
  .cityList--list {
    column-count: 3;
  }
}
@media (max-width: 650px) {
  .cityList--list {
    column-count: 2;
    max-width: 400px;
    margin: auto;
  }
}
@media (max-width: 500px) {
  .cityList--item {
    font-size: 12px;
    line-height: 16px;
  }
  .cityList--item:before {
    font-size: 16px;
  }
}
</style>
