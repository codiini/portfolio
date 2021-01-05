<template>
  <section class="experience_container">
    <div class="experience">
      <h3 class="experience__title">Relevant Experiences</h3>
      <div>
        <ul class="nav nav-tabs nav-justified">
          <li class="nav-item">
            <a
              class="nav-link"
              @click.prevent="setActive('home')"
              :class="{ active: isActive('home') }"
              href="#home"
              >Home</a
            >
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              @click.prevent="setActive('profile')"
              :class="{ active: isActive('profile') }"
              href="#profile"
              >Profile</a
            >
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              @click.prevent="setActive('contact')"
              :class="{ active: isActive('contact') }"
              href="#contact"
              >Contact</a
            >
          </li>
        </ul>
        <div class="tab-content py-3" id="myTabContent">
          <div
            class="tab-pane fade"
            :class="{ 'active show': isActive('home') }"
            id="home"
          >
            Home content
          </div>
          <div
            class="tab-pane fade"
            :class="{ 'active show': isActive('profile') }"
            id="profile"
          >
            Profile content
          </div>
          <div
            class="tab-pane fade"
            :class="{ 'active show': isActive('contact') }"
            id="contact"
          >
            Contact content
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      activeItem: "home",
    };
  },
  methods: {
    isActive(menuItem) {
      return this.activeItem === menuItem;
    },
    setActive(menuItem) {
      this.activeItem = menuItem;
    },
  },
};
</script>