<template>
  <div>
    <div class="container">
      <Header />
      <SectionOne />
      <SectionTwo />
    </div>
    <SectionThree />
    <SectionFour />
    <SectionFive />
    <SectionSix />
    <SectionSeven />
  </div>
</template>

<script>
import SectionSeven from "@/components/Home/SectionSeven";
import SectionSix from "@/components/Home/SectionSix";
import SectionFive from "@/components/Home/SectionFive";
import SectionFour from "@/components/Home/SectionFour";
import SectionThree from "@/components/Home/SectionThree";
import SectionTwo from "@/components/Home/SectionTwo";
import SectionOne from "@/components/Home/SectionOne";
import Header from "@/components/Header";
export default {
  components: {
    Header,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    SectionFive,
    SectionSix,
    SectionSeven
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  max-width: 1170px;
  margin: 0 auto;
}
</style>
