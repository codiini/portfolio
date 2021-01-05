<template>
  <section class="article-section">
    <h1 class="article-section__title">Some Knowledge I've Shared</h1>
    <div class="article">
      <h2>Bem Css; Do’s and Dont’s</h2>
      <img src="@/assets/images/arrow-right.svg" alt="" />
    </div>
    <div class="article">
      <h2>Understanding CSS And the mordern web</h2>
      <img src="@/assets/images/arrow-right.svg" alt="" />
    </div>
    <div class="article">
      <h2>Dealing with imposter syndrome as a developer</h2>
      <img src="@/assets/images/arrow-right.svg" alt="" />
    </div>
    <div class="article">
      <h2>Understanding Template literals in Javascript</h2>
      <img src="@/assets/images/arrow-right.svg" alt="" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.article-section {
  &__title {
    @include sub-heading-text;
    padding: 2rem 0;
  }
  .article {
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: $nyanza;
    width: 100%;
    padding: 2rem 2rem 2rem 0;
    border-bottom: 1px solid $nyanza;
  }
  .article:nth-child(2) {
    border-top: 1px solid $nyanza;
  }
}
</style>