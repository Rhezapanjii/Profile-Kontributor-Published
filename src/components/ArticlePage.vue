<template>
  <div class="article-page d-flex">
    <ArticleNavbar></ArticleNavbar>
    <div class="col col-xl article">
      <ArticleTab></ArticleTab>
      <div class="right-bar">
        <SideBarPublished></SideBarPublished>
      </div>
    </div>
  </div>
</template>

<script>
import ArticleNavbar from './ArticleNavbar.vue'
import ArticleTab from './ArticleTab.vue'
import SideBarPublished from './SideBarPublished.vue'
export default {
  name: 'App',
  components: {
    ArticleNavbar,
    ArticleTab,
    SideBarPublished
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.article-page {
  background-color: #309C9F;
  height: 200vh;
  margin: 0;
}

.article {
  border-radius: 50px 0 0 0;
  background: rgba(245, 245, 245, 1);
  display: flex;
}

.right-bar {
  width: 35%;
  border-radius: 50px 0 0 0;
  background: #fff;
  position: relative;
}
</style>
