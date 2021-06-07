<template>
  <div class="post">
    <div class="post-content">
    <a class="post-header post-header-link clickable">
      <h4 class="title is-4"> {{title}} <br> Гарчиг</h4>
      <h5 class="subtitle is-5"> {{subtitle}}  <br> Дэд гарчиг</h5>
    </a>
    <div class="post-footer">
      by Pvrew-Erdene, {{formatDate()}}
      <br>
    </div>
    </div>
    <div class="post-right">
      <label class="checkbox">
        <input type="checkbox" :checked="isRead">
        Унших
      </label>
    </div>
  </div>
</template>

<script>
import moment from 'moment'
export default {
  props: {
    title: {
      type: String,
      require: true
    },
    subtitle: {
      type: String,
      require: false
    },
    date: {
      type: Date,
      required: false,
      default: new Date()
    },
    isRead: {
      type: Boolean,
      required: false
    }
  },
  methods: {

    formatDate () {
      return moment(this.date).format('LL')
    }
  }
}
</script>

<style scoped lang="scss">
.post-footer{
  font-style: italic;
}
.post-content {
  flex:1;
}
.post {

  margin-bottom: 20px;
  padding: 5px;
  border-bottom: 2px solid transparent;
  display: flex;
  flex-direction: row;
  &-content{
    flex: 1;
  }
  &-right{
    float: right;
    justify-content: flex-end;
    align-self:center;
  }
  &:hover{
  border-bottom: 2px solid #e8e8e8;
}
}
.post-right{
  float: right;
  justify-content: flex-end;
  align-self: center;
}
.post:hover {
  border-bottom: 2px solid #e8e8e8;
}
</style>
