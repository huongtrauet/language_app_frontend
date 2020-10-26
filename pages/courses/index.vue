<template>
  <section class="container">
    <div>
      <h1 class="title">Nguyen Thi Huong Tra {{ $t("welcome") }}</h1>
      <nuxt-link :to="localePath('/login')">
        <a-button type="danger"> Danger </a-button>
      </nuxt-link>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
