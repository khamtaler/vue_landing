<script setup>
import Heading from "./Heading.vue";
import ParallaxPhoto from "./ParallaxPhoto.vue";
</script>
<template>
  <section class="section section---fullWidth section---removeTopDistance">
    <header class="header">
      <img
        alt="Tuoglos logo"
        class="logo"
        src="../assets//images/logo.svg"
        width="125"
        height="125"
      />

      <div class="wrapper">
        <Heading msg="Szukasz pracownika w Polsce lub za granicą?" />
      </div>
    </header>
    <ParallaxPhoto>
      <h2 class="parallaxContainer--boxHeader">
        Wystarczą <b>dwie minuty</b> abyś dodał swoje ogłoszenie do ponad
        <b>100 portali ogłoszeniowych</b> w całej Polsce!
      </h2></ParallaxPhoto
    >
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.section---removeTopDistance {
  margin-top: 0px;
  padding-top: 0px;
}
.logo {
  display: block;
  margin: 30px 0px;
}
.header {
  display: flex;
  flex-direction: column;
  line-height: 1.5;
}

.parallaxContainer--boxHeader {
  font-weight: 100;
  color: #fff;
  text-align: center;
}

@media (min-width: 1024px) {
  .header {
    display: flex;
    width: 100%;
    max-width: 500px;
    margin-left: auto;
  }
  .logo {
    width: 300px;
    height: auto;
  }
}
@media (min-width: 768px) {
  .logo {
    width: 200px;
    height: auto;
  }
}
@media (max-width: 767px) {
  .logo {
    width: 300px;
    height: auto;
    margin: auto;
  }
}
</style>
