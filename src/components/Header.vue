<script setup>
import Heading from "./Heading.vue";
import ParallaxPhoto from "./ParallaxPhoto.vue";
</script>
<template>
  <section class="section section---fullWidth section---noTopMargin">
    <header class="header">
      <img alt="Tuoglos logo" class="logo" src="../assets/logo.svg" width="125" height="125" />

      <div class="wrapper">
        <Heading
          msg="DODAMY TWOJE OGŁOSZENIE
DO PONAD 100 PORTALI OGŁOSZENIOWYCH"
        />
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
.section---noTopMargin {
  margin-top: 0px;
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
</style>
