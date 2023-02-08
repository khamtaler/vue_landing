<script setup>
import ArchiveTile from "./components/ArchiveTile.vue";
import DefaultSection from "./components/DefaultSection.vue";
import Header from "./components/Header.vue";
import ReasonTile from "./components/ReasonTile.vue";
import CitiesList from "./components/CitiesList.vue";
import Data from "./constants/Cities.vue";
import FullStar from "./components/icons/iconFullStar.vue";
import HalfStar from "./components/icons/iconHalfStar.vue";
import IconGlobe from "./components/icons/IconGlobe.vue";
import IconCheck from "./components/icons/IconCheck.vue";
import IconChain from "./components/icons/IconChain.vue";
import IconDocument from "./components/icons/IconDocument.vue";
import PriceCircle from "./components/PriceCircle.vue";
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
          <ArchiveTile class="archiveSection--archiveTile" year="2010r.">
            <img class="archiveSection--image" src="./assets/images/2010.png" alt="Archive 2010" />
          </ArchiveTile>
          <ArchiveTile class="archiveSection--archiveTile" year="2018r."
            ><img class="archiveSection--image" src="./assets/images/2018.png" alt="Archive 2018" />
          </ArchiveTile>

          <ArchiveTile class="archiveSection--archiveTile" year="2020r."
            ><img class="archiveSection--image" src="./assets/images/2020.png" alt="Archive 2020" />
          </ArchiveTile>
          <ArchiveTile class="archiveSection--archiveTile" year="2022r."
            ><img class="archiveSection--image" src="./assets/images/2021.png" alt="Archive 2022" />
          </ArchiveTile>
        </div>
        <p class="archiveSection--rating">
          Jak nasi klienci oceniają naszą usługę:<span class="archiveSection--ratingNumbers"
            >4,89
            <FullStar v-for="i in 4" class="archiveSection--star" />
            <HalfStar class="archiveSection--star" />
          </span>
        </p>
      </div>
    </DefaultSection>
    <DefaultSection
      class="reasonsSection section---fullWidth section---whiteHeader"
      header="Dlaczego warto?"
    >
      <div class="reasonsSection--container">
        <ReasonTile desc="Ponad 100 portali ogłoszeniowych w całej Polsce">
          <IconGlobe class="reasonsSection--icon" />
        </ReasonTile>
        <ReasonTile
          desc="Automatyzujemy proces dodawania ogłoszeń jednocześnie do 100 serwisów. Oszczędzasz czas i unikasz pomyłek."
        >
          <IconCheck class="reasonsSection--icon" />
        </ReasonTile>
        <ReasonTile
          desc="Generujemy automatyczny raport, wysyłając na adres e-mail 100 linków do ogłoszeń na naszych 100 portalach."
        >
          <IconDocument class="reasonsSection--icon"
        /></ReasonTile>
        <ReasonTile
          desc="Umożliwiamy zamieszczanie linków do Twojej strony www - na stronach głównych
i w ogłoszeniach"
        >
          <IconChain class="reasonsSection--icon"
        /></ReasonTile>
      </div>
      <a class="button button---VerticalMargin" href="#/">+ Dodaj ogłoszenie do 100 portali</a>
    </DefaultSection>
    <DefaultSection class="section--citiesList" header="Gdzie opublikujemy Twoje ogłoszenie?">
      <p class="section--citiesListP">
        Grupa Tuogoś to ogólnopolski portal ogłoszeniowy Tuogłoś.pl, regionalne portale:
        naslasku.com i nadolnymslasku.com, wtrojmiescie.com, 100 portali w stu największych miastach
        Polski i 28 portali dla Polaków za granicą.
      </p>
      <CitiesList header="Portale w Polsce" :list="Data.POLISH_CITIES" />
    </DefaultSection>
    <DefaultSection class="section--citiesList">
      <img class="section--citiesListMap" src="./assets/images/polonia.jpg" />
      <CitiesList header="Portale dla Polaków za granicą" :list="Data.WORLD_CITIES" />
    </DefaultSection>
    <DefaultSection class="sectionPricing section---fullWidth">
      <div class="sectionPricing--container">
        <div class="sectionPricing--containerInnerLeft">
          <h3 class="sectionPricing--header">Ile to kosztuje?</h3>
          <p class="sectionPricing--p">
            Tylko 2 minuty zajmie Ci wypełnienie jednego formularza i wybranie miast, w których
            chcesz znaleźć klientów na swoje usługi i towary. Możesz zamieścić ogłoszenie w dowolnej
            ilości serwisów - koszt 50 groszy za 1 miasto, lub dodać je automatycznie do wszystkich
            100 serwisów za jedyne 17 zł. Zwrotnie otrzymasz email z raportem, w którym będą linki
            do wszystkich Twoich ogłoszeń.
          </p>
          <p>Na życzenie wystawiamy faktury VAT.</p>
        </div>
        <div class="sectionPricing--containerInnerRight">
          <div class="sectionPricing--prices">
            <div class="sectionPricing--pricesInner">
              <PriceCircle price="17zł" amount="100 portali" />
              <p class="sectionPricing--pricesInnerP">lub</p>
              <PriceCircle price="50gr" amount="1 portal" />
            </div>
            <p class="sectionPricing--containerInnerRightP">
              Wypełnij formularz i dodaj swoje ogłoszenie wybierając konkretne serwisy lub ogłoś się
              w całej Polsce!
            </p>
          </div>
          <a class="button button---VerticalMargin" href="#/">+ Dodaj ogłoszenie do 100 portali</a>
        </div>
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

.mapSection--image {
  mix-blend-mode: multiply;
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

.archiveSection--image {
  width: 100%;
  height: 300px;
}

.mapSection--image,
.mapSection--paragraph {
  width: 100%;
}
.archiveSection--item:hover {
  overflow: visible;
}

.archiveSection--item:hover .archiveSection--image {
  scale: 1.5;
  z-index: 2;
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

.reasonsSection {
  background: linear-gradient(#002de291 100%, rgba(199, 0, 98, 0.5) 100%),
    url(./assets/images/laptop-woman-2.jpg);
  background-repeat: no-repeat;
  background-position: top center;
  background-size: cover;
  background-attachment: fixed;
}
.reasonsSection--container,
.sectionPricing--container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  max-width: 1000px;
  margin: 50px auto;
  flex-wrap: wrap;
}
.reasonsSection--icon {
  width: 35px;
  height: auto;
  filter: invert(98%) sepia(0%) saturate(0%) hue-rotate(37deg) brightness(102%) contrast(105%);
}
.section--citiesListP {
  text-align: center;
}
.section--citiesListMap {
  width: 80%;
  margin: auto;
}
.sectionPricing {
  background: #002fe2;
  color: #fff;
}
.sectionPricing--header {
  text-align: left;
  font-size: 52px;
  font-weight: 700;
  line-height: 1.2;
}
.sectionPricing--p {
  margin: 30px 0px;
}

.sectionPricing--prices {
  background: #fff;
  color: #000;
  padding: 20px;
  border-radius: 5px;
}
.sectionPricing--pricesInner {
  display: flex;
  width: 100%;
  justify-content: space-around;
  align-items: center;
  margin-bottom: 30px;
}
.sectionPricing--pricesInnerP {
  color: #002de2;
  font-size: 25px;
}
@media (min-width: 1024px) {
  .mapSection--image,
  .mapSection--paragraph {
    width: 50%;
  }
  .archiveSection--image {
    width: 100%;
    height: 250px;
  }
  .sectionPricing--containerInnerLeft {
    width: 55%;
  }
  .sectionPricing--containerInnerRight {
    width: 40%;
    text-align: center;
  }
}

@media (max-width: 1023px) {
  .archiveSection--image {
    width: 100%;
    height: 250px;
  }
  .mapSection--mapContainer {
    width: 70%;
  }
  .sectionPricing--header {
    text-align: center;
  }
  .sectionPricing--prices {
    max-width: 70%;
    margin: 20px auto 10px;
  }
}
@media (max-width: 768px) {
  .archiveSection--item {
    width: 46%;
  }
  .archiveSection--image {
    width: 100%;
    height: 250px;
  }
  .mapSection--mapContainer {
    width: 100%;
    flex-direction: column;
  }
  .mapSection--paragraph {
    margin: auto;
    text-align: center;
  }
  .reasonsSection--container {
    margin-top: 0px;
  }
  .sectionPricing--container {
    margin-bottom: 0px;
  }
}
@media (max-width: 500px) {
  .sectionPricing--prices {
    max-width: 90%;
  }
}
</style>
