<template>
  <div>
    <Nav />
    <div class="main_content">
      <Hero />
      <About />
      <!-- <Experience /> -->
      <Projects />
      <Articles />
      <Contact />
    </div>
  </div>
</template>

<script>
import Nav from "@/components/include/Nav";
import Hero from "@/components/sections/Hero";
import About from "@/components/sections/About";
// import Experience from "@/components/sections/Experience";
import Articles from "@/components/sections/Articles";
import Projects from "@/components/sections/Projects";
import Contact from "@/components/sections/Contact";
export default {
  components: {
    Nav,
    Hero,
    About,
    // Experience,
    Articles,
    Projects,
    Contact,
  },
};
</script>

<style lang="scss">
.main_content {
  padding: 0 100px;
}
section {
  padding: 30px 0;
}
.social_links ul {
  @include basic-flex;
  height: 100px;
  padding: 0 20px;
}
.twitter-icon,
.github-icon,
.linkedin-icon {
  stroke: $white-text;
}
</style>
