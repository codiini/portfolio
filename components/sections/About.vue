<template>
  <section class="about_container">
    <div class="about">
      <h3 class="about__title">About Me</h3>
      <div>
        <div class="about__description">
          <p>Hello! I'm Iniubong, a software engineer based in Nigeria.</p>
          <p>
            I enjoy creating things that live on the internet, whether that be
            websites, applications, or anything in between. My goal is to always
            build products that provide pixel-perfect, performant experiences.
          </p>
          <p>
            <!-- Shortly after graduating from University of Nigeria, I joined the
            engineering team at Upstatement where I work on a wide variety of
            interesting and meaningful projects on a daily basis. -->
          </p>
        </div>
      </div>
      <div class="proficient_tools">
        <h2 class="about__sub-title">
          Tools and Languages I'm proficient with:
        </h2>
        <ul class="about__skills">
          <li v-for="(skill, index) in skills" :key="index" class="skills_list">
            {{ skill.language }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.about {
  max-width: 800px;
  color: $nyanza;
  height: 60vh;
  &__title {
    @include sub-heading-text;
  }
  &__description {
    color: $nyanza;
  }
  &__skills {
    display: grid;
    grid-template-columns: repeat(2, minmax(200px, 300px));
    padding: 0;
    margin: 20px 0 0;
    overflow: hidden;
    list-style: none;
    p {
      margin-bottom: 15px;
    }
  }
  &__sub-title {
    @include sub-heading-text;
    margin-top: 30px;
  }
}
.skills_list {
  margin: 5px 0;
  &:before {
    content: "▹";
  }
}
.proficient_tools {
  margin-top: 50px;
}
</style>

<script>
export default {
  name: "About",
  data() {
    return {
      skills: [
        {
          language: "HTML",
        },
        {
          language: "CSS",
          icon: "",
        },
        {
          language: "Javascript (ES6+)",
        },
        {
          language: "SCSS",
          icon: "",
        },
        {
          language: "Vuejs",
        },
        {
          language: "Nuxtjs",
          icon: ``,
        },
      ],
    };
  },
  computed: {
    // avatar() {
    //  return this.$cloudinary().url(`samples/landscapes/girl-urban-view.jpg`, {
    //       width: 100,
    //       height: 100,
    //       radius: 'max',
    //       crop: 'thumb'
    //    })
    //   }
  },
};
</script>