<template>
  <section class="top-content">
    <div class="hero">
      <p class="hero__intro">Hi! 👋🏿 my name is</p>
      <h1 class="hero__name">Iniubong Obonguko.</h1>
      <h2 class="hero__title">Web developer extraordinaire.</h2>
      <p class="hero__bio">
        I'm a software engineer based in Uyo, Nigeria specializing in building
        exceptional websites, applications and everything in between.
      </p>
      <a href="mailto:iniubongobonguko2018@gmail.com" class="hero__btn">Let's talk</a>
    </div>
    
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.top-content {
  @include basic-flex;
}
.hero {
  padding-top:100px;
  height: 100vh;
  &__intro {
    color: $white-text;
    font-weight: 400;
  }
  &__name {
    color: $white-text;
    font-weight: 700;
    font-size: clamp(40px, 8vw, 80px);
  }
  &__title {
    font-weight: 400;
    font-size: clamp(20px, 3vw, 30px);
    color: $ocean-green;
    margin-bottom: 10px;
  }
  &__bio {
    color: $ocean-green;
    width: 60%;
    margin-top: 2rem;
  }
  &__btn {
    display: inline-block;
    padding: 0.7rem 3rem;
    margin-top: 5rem;
    text-align: center;
    background: transparent;
    border: 1px solid $light-blue;
    color: $nyanza;
    &:hover {
      background-color: $deep-blue;
      color: #fff;
      transition: 0.3s ease-in-out;
    }
  }
}
@media screen and (max-width:700px) {
  .social_links{
    display: none;
  }
  .hero__bio{
    width:100%;
  }
}
</style>
