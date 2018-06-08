<template>
  <div class="sidebar pure-u-1 pure-u-md-1-4">
    <div class="header">
      <a href="/">
        <img src="header.png" alt="" srcset="">
      </a>
      <a href="/">
      <h1 class="brand-title">大章鱼</h1>
      </a>
      <h2 class="brand-tagline">
        留一些时间，多一些思考
      </h2>
      <nav class="nav">
        <ul class="nav-list">
          <li class="nav-item">
            <a class="pure-button" href="/files/">归档</a>
          </li>
          <li class="nav-item">
            <a class="pure-button" href="/categorys/">分类</a>
          </li>
          <li class="nav-item">
            <a class="pure-button" href="/friendlinks/">友链</a>
          </li>
          <br>
          <form method="get" action="/search/" style="margin-top: 1em;" class="pure-form">
            <input type="search" style="color: #3d4f5d; margin-left: 15%; margin-right: 15%; width: 70%" placeholder="搜索">
          </form>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
import '@/common/css/pure-min.css'
import '@/common/css/monokai.css'
import '@/common/css/grids-responsive-min.css'
import '@/common/css/blog.css'
export default {

}
</script>

<style scoped>

</style>
