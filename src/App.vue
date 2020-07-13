<template>
  <MainView>
    <template v-slot:header>
      <Header class="full-width main-header" id="header" />
    </template>
    <template v-slot:about>
      <About class="full-width" style="margin-top:20px;" id="about" />
    </template>
    <template v-slot:skills>
      <Skills class="full-width" id="skill" />
    </template>
    <template v-slot:certificate>
      <Certificate class="full-width" id="certificate" />
    </template>
    <template v-slot:projects>
      <Projects class="full-width" id="project" />
    </template>
    <template v-slot:footer>
      <Footer class="full-width main-footer" id="footer" />
    </template>
  </MainView>
</template>

<script>
import MainView from "@/views/MainView";
import Header from "@/components/Header";
import Footer from "@/components/Footer";
import About from "@/components/About";
import Skills from "@/components/Skills";
import Certificate from "@/components/Certificates";
import Projects from "@/components/Projects.vue";

export default {
  name: "App",
  components: {
    Header,
    Projects,
    MainView,
    Footer,
    About,
    Skills,
    Certificate
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.full-width {
  width: 100%;
}
.main-footer {
  position: absolute;
  bottom: 0;
  height: 15%;
}
.main-header {
  position: absolute;
  top: 0;
  height: 15%;
}
</style>
