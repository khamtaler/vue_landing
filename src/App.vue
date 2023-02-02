<script setup>
import ArchiveTile from "./components/ArchiveTile.vue";
import DefaultSection from "./components/DefaultSection.vue";
import Header from "./components/Header.vue";
import FullStar from "./components/icons/iconFullStar.vue";
import HalfStar from "./components/icons/iconHalfStar.vue";
</script>

<template>
  <Header />
  <main>
    <DefaultSection class="mapSection" header="Jak to działa?">
      <div>
        <p>
          Tuogłoś.pl to jedyny w Polsce portal z ogłoszeniami drobnymi, ogłoszeniami nieruchomości,
          ofertami pracy, ogłoszeniami auto-moto, który umożliwia automatyczną publikację Twojego
          ogłoszenia w <b>100 portalach</b> ogłoszeniowych w stu największych miastach Polski.
        </p>
        <div class="mapSection--mapContainer">
          <img class="mapSection--image" src="./assets/images/mapa-nowa.png" />
          <p class="mapSection--paragraph">
            Możesz wybrać dowolną ilość portali lub dodać automatycznie swoje ogłoszenie do
            wszystkich stu serwisów.
          </p>
        </div>
      </div>
    </DefaultSection>
    <DefaultSection class="archiveSection" header="Jak zmienialiśmy sie na przestrzeni lat?">
      <div>
        <p class="archiveSection--intro">
          Wszystkie portale Grupy Tuogłoś mają ugruntowaną pozycję wśród polskich serwisów
          ogłoszeniowych i działają w sposób nieprzerwany od <b>ponad 10 lat</b>. Z roku na rok
          zwiększamy funkcjonalność serwisów, automatyzujemy publikację ogłoszeń i reklam, jesteśmy
          coraz bardziej efektywni i przynosimy naszym użytkownikom coraz więcej korzyści
          umożliwiając skuteczną sprzedaż ich towarów i usług.
        </p>
        <div class="archiveSection--archive">
          <ArchiveTile
            class="archiveSection--archiveTile"
            year="2010r."
            fileName="2010.png"
            altText="Archive 2010"
          >
          </ArchiveTile>
          <ArchiveTile
            class="archiveSection--archiveTile"
            year="2018r."
            fileName="2018.png"
            altText="Archive 2018"
          >
          </ArchiveTile>

          <ArchiveTile
            class="archiveSection--archiveTile"
            year="2020r."
            fileName="2020.png"
            altText="Archive 2020"
          >
          </ArchiveTile>
          <ArchiveTile
            class="archiveSection--archiveTile"
            year="2022r."
            fileName="2021.png"
            altText="Archive 2022"
          >
          </ArchiveTile>
        </div>
        <p class="archiveSection--rating">
          Jak nasi klienci oceniają naszą usługę:<span class="archiveSection--ratingNumbers"
            >4,89
            <FullStar class="archiveSection--star" />
            <FullStar class="archiveSection--star" />
            <FullStar class="archiveSection--star" />
            <FullStar class="archiveSection--star" />
            <HalfStar class="archiveSection--star" />
          </span>
        </p>
      </div>
    </DefaultSection>
  </main>
</template>

<style scoped>
.mapSection--mapContainer {
  display: flex;
  align-items: center;
  margin: 30px 0px;
}
.mapSection--image,
.mapSection--paragraph {
  width: 50%;
}
.mapSection--paragraph {
  margin-left: 30px;
}
.archiveSection--archive {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 50px;
}

.archiveSection--rating {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 30px;
}
.archiveSection--ratingNumbers {
  color: #002de2;
  margin-left: 10px;
  font-size: 28px;
  font-weight: 500;
  line-height: 1.6;
  display: flex;
  align-items: center;
  justify-content: center;
}
.archiveSection--star {
  width: 20px;
  filter: invert(12%) sepia(99%) saturate(7047%) hue-rotate(235deg) brightness(86%) contrast(109%);
}
.archiveSection--star:first-child {
  margin-left: 8px;
}
</style>
