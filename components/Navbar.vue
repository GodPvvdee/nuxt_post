<template>
  <nav class="navbar has-shadow">
    <div class="container">
      <div class="navbar-brand">
        <a class="navbar-item" href="../">
          <img
            src="https://bulma.io/images/bulma-logo.png"
            alt="Lalriin logogogogogogo"
          >
        </a>
        <div
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navMenu"
        >
          <span />
          <span />
          <span />
        </div>
      </div>
      <div @click="isActive =!isActive" id="navMenu" class="navbar-menu">
        <div class="navbar-end">
          <div
            :class="{'is-active': isActive}"
            class="navbar-item has-dropdown ">
            <a class="navbar-link">Цэс</a>
            <div class="navbar-dropdown">
              <nuxt-link to="/" class=" navbar-item">Нүүр</nuxt-link>
              <nuxt-link to="/manage" class=" navbar-item">Удирдах</nuxt-link>
<!--              <hr class="navbar-divider">-->
<!--              <div class="navbar-item">-->
<!--                Log out-->
<!--              </div>-->
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      isActive: false
    }
  }
}
</script>

<style></style>
