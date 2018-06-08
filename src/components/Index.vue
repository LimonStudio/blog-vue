<template>
  <div class="content pure-u-1 pure-u-md-3-4">
    <!-- A wrapper for all the blog posts -->
    <div class="posts">
      <section class="post" v-for="(item, index) in articles" :key="index">
        <header class="post-header">
          <h2 class="post-title">
            <a href="/article/6">{{item.fields.blog_article_title}}</a>
          </h2>
          <p class="post-meta">
            发布时间:
            <span>{{item.fields.blog_article_publish_time}}</span>
            浏览次数:
            <span>{{item.fields.blog_article_click_count}}</span>
            点赞次数:
            <span>{{item.fields.blog_article_agree_count}}</span>
          </p>
        </header>
        <div class="post-description">
          <p>
            {{item.fields.blog_article_content.substr(0, 150)}}
            <a style="font-weight: inherit" href="/article/6">
              Read More
            </a>
          </p>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
      headTitle: '',
      userDesc: '',
      userName: '',
      articles: []
    }
  },
  created () {
    axios.get('/articleApi').then(({data}) => {
      this.headTitle = data.head_title
      this.userDesc = data.user_desc
      this.userName = data.user_name
      this.articles = data.articles
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
