<template>
  <div>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bulma@0.9.2/css/bulma.min.css"
    />
    <navbar />
    <manage/>
    <div class="blogs-page">
      <div class="main-content">
        <div class="container">
          <div class="columns is-mobile">
            <div class="column is-8 is-offset-2">
              <div class="section">
                <div class="title">
                  <h1>Шинэ мэдээ</h1>
                  <hr />
                </div>
                <post-item
                  v-for="post in posts"
                  :key="post._id"
                  :title="post.title"
                  :subtitle="post.subtitle"
                  :date="post.date"
                  :isRead="post.isRead"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
<!--      <form>-->
<!--        -->
<!--      </form>-->
    </div>
  </div>
</template>

<script>
// import Postitem from "~/components/PostItem.vue";
// import Postitem from "~/components/PostItem.vue";
export default {

  data () {
    return {
      title: 'hi'
    }
  },
  computed: {
    posts () {
      return this.$store.state.posts
    }
  }
}
</script>
<style>

</style>
