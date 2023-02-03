<script setup>
defineProps({
  price: {
    type: String,
    required: true,
  },
  amount: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="priceCircle">
    <h4 class="priceCircle--price">{{ price }}</h4>
    <hr class="priceCircle--line" />
    <h5 class="priceCircle--amount">{{ amount }}</h5>
  </div>
</template>

<style scoped>
.priceCircle {
  border: 2px solid #002fe2;
  color: #002fe2;
  padding: 10px;
  border-radius: 50%;
  width: 35%;
  aspect-ratio: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.priceCircle--price {
  font-size: 28px;
  line-height: 100%;
  font-weight: 700;
}
.priceCircle--line {
  height: 1px;
  width: 60px;
  margin: 10px auto;
  border: #002de2 1px solid;
}
.priceCircle--amount {
  font-size: 20px;
  line-height: 100%;
}
</style>
