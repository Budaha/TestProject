<template>
  <header class="home" id="home">
    <homeSectionComponent class="container" />
  </header>
  <div class="about-us" id="about-us">
    <aboutUsComponent class="container" />
  </div>
  <div class="company">
    <companyComponent class="container" />
  </div>
  <div class="definition">
    <definitionComponent class="container" />
  </div>
  <div class="services" id="services">
    <servicesComponent class="container" />
  </div>
  <div class="stages">
    <stagesComponent class="container" />
  </div>
  <div class="documents">
    <documentsComponent />
  </div>
  <div class="risks">
    <risksComponent class="container" />
  </div>
  <div class="results">
    <resultsComponent class="container" />
  </div>
  <div class="urgent">
    <urgentProcessingComponent class="container" />
  </div>
  <div class="slider-stages">
    <sliderStagesComponent class="container" />
  </div>
  <div class="other-services">
    <otherServicesComponent class="container" />
  </div>
  <div class="people">
    <peopleComponent class="container" />
  </div>
  <div class="input" id="input">
    <inputComponent class="container" />
  </div>
  <div class="footer">
    <footerComponent class="container" />
  </div>
</template>

<script>
import homeSectionComponent from "@/components/HomeSection.vue";
import aboutUsComponent from "@/components/AboutUsComponent.vue";
import companyComponent from "@/components/CompanyComponent.vue";
import definitionComponent from "@/components/DefinitionComponent.vue";
import servicesComponent from "@/components/ServicesComponent.vue";
import stagesComponent from "@/components/StagesComponent.vue";
import documentsComponent from "@/components/DocumentsComponent.vue";
import risksComponent from "@/components/RisksComponent.vue";
import resultsComponent from "@/components/ResultsComponent.vue";
import urgentProcessingComponent from "@/components/UrgentProcessingComponent.vue";
import sliderStagesComponent from "@/components/SliderStagesComponent.vue";
import otherServicesComponent from "@/components/OtherServicesComponent.vue";
import peopleComponent from "@/components/PeopleComponent.vue";
import inputComponent from "@/components/InputComponent.vue";
import footerComponent from "@/components/FooterComponent.vue";

export default {
  components: {
    homeSectionComponent,
    aboutUsComponent,
    companyComponent,
    definitionComponent,
    servicesComponent,
    stagesComponent,
    documentsComponent,
    risksComponent,
    resultsComponent,
    urgentProcessingComponent,
    sliderStagesComponent,
    otherServicesComponent,
    peopleComponent,
    inputComponent,
    footerComponent,
  },
  data() {
    return {
    };
  },
};
</script>

<style lang="scss">
.home {
  padding-bottom: 105px;
  background: url("/src/assets/img/Rectangle 1.png");
  @media (max-width: 768px) {
    padding-bottom: 60px;
  }
}
.about {
  @media (max-width: 1200px) {
    display: flex;
    flex-direction: column;
  }
}
.company {
  padding-top: 120px;
  padding-bottom: 120px;
  background-color: #222423;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 60px;
  }
  @media (max-width: 500px) {
    padding-top: 30px;
    padding-bottom: 40px;
  }
}
.definition {
  background-color: #ffffff;
  padding-top: 120px;
  @media (max-width: 1200px) {
    padding-top: 60px;
  }
  @media (max-width: 500px) {
    padding-top: 30px;
    padding-bottom: 40px;
  }
}
.services {
  background-color: #ffffff;
  padding-top: 119px;
  @media (max-width: 1200px) {
    padding-top: 60px;
  }
  @media (max-width: 500px) {
    padding-top: 20px;
    padding-bottom: 40px;
  }
}
.stages {
  background-color: #222423;
  margin-top: -125px;
  padding-bottom: 121px;
  @media (max-width: 1440px) {
    margin-top: -20px;
  }
}
.documents {
  background: url("/src/assets/img/docSection.png");
  background-position: right;
  background-repeat: no-repeat;
  opacity: 90%;
  @media (max-width: 1024px) {
    background: none;
  }
}
.risks {
  background-color: #ffffff;
  padding-top: 120px;
  padding-bottom: 120px;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 60px;
  }
  @media (max-width: 768px) {
    padding-top: 20px;
  }
}
.results {
  background-color: #222423;
  padding-top: 120px;
  padding-bottom: 120px;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 60px;
  }
}
.urgent {
  background-color: #ffffff;
  padding-top: 120px;
  padding-bottom: 120px;
  @media (max-width: 768px) {
    padding-top: 60px;
    padding-bottom: 60px;
  }
}
.slider-stages {
  background-color: #222423;
  padding-top: 100px;
  padding-bottom: 123px;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 60px;
  }
}
.other-services {
  background-color: #ffffff;
  padding-bottom: 50px;
}
.people {
  background-color: #222423;
  padding-top: 100px;
  padding-bottom: 100px;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 0px;
  }
}
.input {
  background-color: #222423;
  padding-top: 110px;
  padding-bottom: 30px;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 0px;
  }
}
.footer {
  background-color: #222423;
  padding-top: 40px;
  padding-bottom: 40px;
  @media (max-width: 768px) {
    padding-top: 30px;
    padding-bottom: 20px;
  }
}
.hidden {
  display: none;
}
</style>
