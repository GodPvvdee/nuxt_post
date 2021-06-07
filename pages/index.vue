<template>
  <div>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bulma@0.9.2/css/bulma.min.css"
    />
    <navbar />
    {{title}}
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
                  v-bind:title="title"
                  v-bind:subtitle="'New Post Subtitle'"
                />
                <post-item
                  v-bind:title="'New Post Title2'"
                  v-bind:subtitle="'New Post Subtitle2'"
                />

              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import Postitem from "~/components/PostItem.vue";
// import Postitem from "~/components/PostItem.vue";
export default {

  data () {
    return {
      title: 'this is fucking title'
    }
  }
}
</script>

<style scoped>
.post-content {
  font-style: italic;
}
.post {
  margin-bottom: 20px;
  padding: 5px;
  border-bottom: 2px solid transparent;
}
.post:hover {
  border-bottom: 2px solid #e8e8e8;
}
</style>
