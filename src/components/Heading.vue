<script setup>
import IconPeople from "./icons/IconPeople.vue";
import IconGlobe from "./icons/IconGlobe.vue";
import IconClock from "./icons/IconClock.vue";

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
    <h2 class="greetings--secondHeader">Z Grupą ogłoszeniową Tuogłoś znajdziesz ich bez trudu!</h2>
    <ul class="greetings--list">
      <li class="greetings--listItem">
        <IconPeople class="greetings--icon" />
        <span class="greetings--listItemText"
          >Użytkownicy naszych portali to potencjalni pracownicy z największych 105 miejscowości
          Polski oraz Polacy za granicą szukający pracy w największych 28 ośrodkach polonijnych na
          świecie</span
        >
      </li>

      <li class="greetings--listItem">
        <IconClock class="greetings--icon" />
        <span class="greetings--listItemText"
          >Zaoszczędzisz swój czas, gdyż nasz system doda za Ciebie ogłoszenie do wszystkich lub
          wybranych serwisów Grupy</span
        >
      </li>
    </ul>

    <a class="button button---VerticalMargin" href="#/">+ Dodaj ogłoszenie do 100 portali</a>
  </div>
</template>

<style scoped>
.greetings--header {
  color: #000;
  font-weight: 500;
  font-size: 1.8rem;
  line-height: 2.2rem;
  padding: 30px 0px;
}
.greetings--list {
  margin: 0px 0px 30px 0px;
  text-decoration: none;
  text-align: start;
}
.greetings--listItem {
  display: flex;
  font-size: 1.2rem;
  margin: 5px 0;
  list-style: none;
}

.greetings--listItemText {
  color: #000;
  font-weight: 500;
  max-width: 80%;
  margin: 15px 0px;
}
.greetings--icon {
  width: 30px;
  margin-right: 8px;
  filter: invert(12%) sepia(99%) saturate(7047%) hue-rotate(235deg) brightness(86%) contrast(109%);
}

.greetings--header {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings {
    margin-right: 50px;
  }
  .greetings--header {
    text-align: left;
  }
  .greetings--icon {
    width: 45px;
    margin-right: 20px;
  }
}
@media (max-width: 1024px) {
  .greetings {
    text-align: center;
  }
  .greetings--header {
    text-align: center;
    padding: 30px;
  }
  .greetings--list {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 800px;
    margin: 30px auto;
  }
  .greetings--listItem {
    padding: 0px 15px;
    justify-content: center;
  }
  .greetings--listItemText {
    max-width: 80%;
  }
}
@media (max-width: 500px) {
  .greetings--header {
    font-size: 1.4rem;
    line-height: 1.7rem;
  }
  .greetings--listItem {
    font-size: 1rem;
  }
  .greetings--listItemText {
    margin-left: 10px;
  }
}
</style>
