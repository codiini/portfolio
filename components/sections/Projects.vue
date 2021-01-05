<template>
  <div class="projects_container">
    <h3 class="projects__title">Some Things I've Built</h3>
    <section class="projects">
      <template v-for="project in projects">
        <div class="project" :key="project.id">
          <h2 class="project_title">{{ project.title }}</h2>
          <p class="project_description">{{ project.description }}</p>
          <div class="project_image">
            <a href="">
              <img
                src="@/assets/images/demo.png"
                alt=""
              />
            </a>
          </div>

          <div class="project_tech">
            <p>Technologies Used:</p>
            <ul class="tech_list">
              <li v-for="(tech, key) in project.techUsed" :key="key">
                {{ tech }}
              </li>
            </ul>
          </div>
        </div>
      </template>
    </section>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.projects {
  margin: 0 auto;
  column-count: 2;
  column-gap: 3.2em;
  &__title {
    @include sub-heading-text;
  }
  .project {
    height: 700px;
    width: 100%;
    max-width: 500px;
    margin: 0 auto 20px auto;
    // border-radius: 10px;
    background-color: #a8b2d1;
    overflow: hidden;
    margin: 3em 0 0 0;
    &_title {
      color: #fff;
      font-size: 20px;
      font-weight: 800;
      text-transform: uppercase;
      padding: 20px;
    }
    &_description {
      padding: 5px 20px;
      font-size: clamp(15px, 20px, 25px);
      font-weight: 700;
      color: rgb(250, 208, 20);
    }
    &_image {
      @include basic-flex;
      max-width: 500px;
      width: 100%;
      margin: 0 auto;
      position: relative;
      right: -50px;
      padding: 30px 0;
      img {
        height: auto;
      }
    }
    &_tech {
      white-space: nowrap;
      padding: 10px 20px;
      p {
        font-weight: 600;
        color: rgb(250, 208, 20);
      }
      .tech_list {
        @include basic-flex;
        li {
          margin: 10px;
          color: $deep-blue;
        }
      }
    }
  }
}

/* projects on small screens */
@media only screen and (max-width: 1000px) {
  .projects {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
}
</style>

<script>
export default {
  name: "projects",
  data() {
    return {
      projects: [
        {
          id: "1",
          title: "Ip address tracker",
          description:
            "Check the IP address, location, timezone and ISP of any URL",
          image:
            "@/components/sections/featured-projects/ip-address-tracker/demo.png",
          techUsed: ["Vuejs", "Vue Router", "Ipfiy API", "Mapbox API"],
          liveUrl: "https://ipaddress-tracker.vercel.app",
          codeRepo: "https://github.com/codini/ip-address-tracker",
        },
        {
          id: "2",
          title: "Ip address tracker",
          description:
            "Check the IP address, location, timezone and ISP of any URL",
          image:
            "@/components/sections/featured-projects/ip-address-tracker/demo.png",
          techUsed: ["Vuejs", "Vue Router", "Ipfiy API", "Mapbox API"],
          liveUrl: "https://ipaddress-tracker.vercel.app",
          codeRepo: "https://github.com/codini/ip-address-tracker",
        },
        {
          id: "3",
          title: "Ip address tracker",
          description:
            "Check the IP address, location, timezone and ISP of any URL",
          image:
            "@/components/sections/featured-projects/ip-address-tracker/demo.png",
          techUsed: ["Vuejs", "Vue Router", "Ipfiy API", "Mapbox API"],
          liveUrl: "https://ipaddress-tracker.vercel.app",
          codeRepo: "https://github.com/codini/ip-address-tracker",
        },
        {
          id: "4",
          title: "Ip address tracker",
          description:
            "Check the IP address, location, timezone and ISP of any URL",
          image:
            "@/components/sections/featured-projects/ip-address-tracker/demo.png",
          techUsed: ["Vuejs", "Vue Router", "Ipfiy API", "Mapbox API"],
          liveUrl: "https://ipaddress-tracker.vercel.app",
          codeRepo: "https://github.com/codini/ip-address-tracker",
        },
      ],
    };
  },
};
</script>