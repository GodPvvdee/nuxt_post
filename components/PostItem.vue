<template>
  <div class="post">
    <a class="post-header post-header-link clickable">
      <h4 class="title is-4"> {{title}} <br> Гарчиг</h4>
      <h5 class="subtitle is-5"> {{subtitle}}  <br> Дэд гарчиг</h5>
    </a>
    <div class="post-content">
      by Pvrew-Erdene, 4th , Jun, 2021
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      require: true
    },
    subtitle: {
      type: String,
      require: false
    }
  }
}
</script>

<style></style>
