<template>
  <div id="app">
    <div class="container">
      <Header @isOpenPopup="onBurger" />
      <Popup :isOpen="isOpen" />
      <SectionStart />
      <SectionFeatures />
      <SectionPlan />
      <SectionGlobal />
      <SectionReview />
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Popup from "./components/Popup.vue";
import SectionStart from "./components/SectionStart.vue";
import SectionFeatures from "./components/SectionFeatures";
import SectionPlan from "./components/SectionPlan";
import SectionGlobal from "./components/SectionGlobal";
import SectionReview from "./components/SectionReview";
import Footer from './components/Footer'
export default {
  name: "App",
  data() {
    return {
      isOpen: false,
    };
  },
  components: {
    Header,
    Popup,
    SectionStart,
    SectionFeatures,
    SectionPlan,
    SectionGlobal,
    SectionReview,
    Footer
  },
  methods: {
    onBurger(data) {
      this.isOpen=data
      console.log(this.isOpen,'app')
    },
  },
};
</script>
