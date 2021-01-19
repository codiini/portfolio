<template>
  <section class="projects_container">
    <h3 class="projects__title">Some Things I've Built</h3>
    <div class="projects">
      <template v-for="project in projects">
        <div class="project" :key="project.id">
          <h2 class="project_title">{{ project.title }}</h2>
          <p class="project_description">{{ project.description }}</p>
          <div class="project_image">
            <a href="">
              <img src="@/assets/images/demo.png" alt="" />
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
    </div>
  </section>
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
.projects_container {
  margin-top: 200px;
}
.projects {
  margin: 0 auto;
  column-count: 2;
  column-gap: 3.2em;
  &__title {
    @include sub-heading-text;
    text-align: left;
    display: flex;
    align-items: flex-end;
  }
  .project {
    height: 700px;
    width: 100%;
    max-width: 500px;
    margin: 0 auto 20px auto;
    background-color: $ocean-green;
    overflow: hidden;
    margin: 3em 0 0 0;
    &_title {
      color: #172a45;
      font-size: 20px;
      font-weight: 800;
      text-transform: uppercase;
      padding: 20px;
    }
    &_description {
      padding: 5px 20px;
      font-size: clamp(15px, 20px, 25px);
      font-weight: 700;
      color: #0f3057;
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
        color: rgb(0, 0, 0);
      }
      .tech_list {
        @include basic-flex;
        li {
          margin: 10px;
          color: #020c1b;
        }
      }
    }
  }
}

/* projects on small screens */
@media only screen and (max-width: 700px) {
  .projects {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    column-gap: 1em;
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