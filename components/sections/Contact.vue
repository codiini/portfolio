<template>
  <section class="contact">
    <h3 class="contact__title">Get in touch</h3>
    <p class="contact__short-text">
      If you like what you see on my portfolio and you think i'd be a great fit
      for a role or you just want to have a friendly chat, my inbox is open
    </p>
    <a href="mailto:iniubongobonguko2018@gmail.com" class="contact__hi-btn"
      >Say Hi</a
    >
    <SocialMedia class="social_media" />
  </section>
</template>

<style lang="scss" scoped>
.social_link {
  margin-right: 40px;
}
.contact {
  max-width: 600px;
  margin: 0 auto;
  text-align: center;
  &__title {
    @include sub-heading-text;
  }
  &__short-text {
    color: $nyanza;
    font-size: 1rem;
  }
  &__hi-btn {
    display: inline-block;
    padding: 0.7rem 3rem;
    margin: 25px 10px;
    border: 1px solid $light-blue;
    color: $nyanza;
    &:hover {
      background-color: $deep-blue;
      color: #fff;
      transition: 0.3s ease-in-out;
    }
  }
  @media screen and (max-width: 700px) {
    .social_links {
      display: block;
      position: relative;
      ul {
        display: flex;
        flex-direction: row;
      }
    }
  }
}
</style>

<script>
import SocialMedia from "@/components/include/SocialMedia";
export default {
  components: {
    SocialMedia,
  },
};
</script>