<script setup>
import IconCheck from "./icons/IconCheck.vue";
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="greetings">
    <h1 class="greetings--header">{{ msg }}</h1>
    <ul class="greetings--list">
      <li class="greetings--listItem"><IconCheck class="checkIcon" /> Oszczędzisz swój czas</li>
      <li class="greetings--listItem">
        <IconCheck class="checkIcon" />Zdobędziesz nowych klientów
      </li>
      <li class="greetings--listItem"><IconCheck class="checkIcon" />Będziesz sprzedawał więcej</li>
    </ul>
    <a class="button button---VerticalMargin" href="#/">+ Dodaj ogłoszenie do 100 portali</a>
  </div>
</template>

<style scoped>
.greetings--header {
  color: #000;
  font-weight: 500;
  font-size: 2.2rem;
  line-height: 2.6rem;
  padding: 30px 50px 30px 0px;
}
.greetings--list {
  margin: 0px 0px 30px 0px;
  text-decoration: none;
  text-align: start;
}
.greetings--listItem {
  display: flex;
  font-size: 1.5rem;
  margin: 5px 0;
  color: #000;
  font-weight: 500;
  list-style: none;
}
.checkIcon {
  width: 30px;
  margin-right: 8px;
  filter: invert(12%) sepia(99%) saturate(7047%) hue-rotate(235deg) brightness(86%) contrast(109%);
}

.greetings--header {
  text-align: center;
}
.button---VerticalMargin {
  display: inline-block;
  margin: 20px 0px;
}

@media (min-width: 1024px) {
  .greetings--header {
    text-align: left;
  }
}
</style>
