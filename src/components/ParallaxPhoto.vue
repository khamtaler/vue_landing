<script setup></script>

<template>
  <div class="parallaxContainer">
    <div class="parallaxContainer--box">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.parallaxContainer {
  width: 50%;
  background-image: url(../assets/images/headerImage.jpg);
  background-repeat: no-repeat;
  background-position: top right;
  background-size: 50% auto;
  background-attachment: fixed;
}
.parallaxContainer--box {
  position: absolute;
  width: 45%;
  padding: 70px 45px;
  bottom: 0;
  left: 0;
  background-color: #002de2b2;
}

@media (max-width: 1024px) {
  .parallaxContainer {
    display: none;
  }
}
</style>
