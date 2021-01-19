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
      <SocialMedia />
    </div>
  </div>
</template>

<script>
import Nav from "@/components/include/Nav";
import Hero from "@/components/sections/Hero";
import SocialMedia from "@/components/include/SocialMedia";
import About from "@/components/sections/About";
import Projects from "@/components/sections/Projects";
import Articles from "@/components/sections/Articles";
import Contact from "@/components/sections/Contact";
export default {
  components: {
    Nav,
    Hero,
    SocialMedia,
    About,
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
.social_links {
  position: fixed;
  width: 100px;
  height: 200px;
  right: 0;
  bottom: 0%;
  ul {
    @include basic-flex;
    height: 100px;
    padding: 0 20px;
    flex-direction: column;
  }
}
.twitter-icon,
.github-icon,
.linkedin-icon {
  stroke: $white-text;
}
@media screen and (min-width: 700px) and (max-width: 900px) {
  .main_content {
    padding: 0 50px;
  }
}
@media screen and (max-width: 700px) {
  .main_content {
    padding: 0 25px;
  }
  section {
    padding: 30px 0;
  }
  .social_links {
    display: none;
  }
}
</style>
