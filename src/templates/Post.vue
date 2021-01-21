<template>
  <Layout>
    <div>
      <h1>Post Page</h1>
      <h2>{{ $page.post.title }}</h2>
      <div>{{ $page.post.content }}</div>
    </div>
  </Layout>
</template>

<page-query>
query ($id: ID!){
  post (id: $id){
    id
    title
    content
  }
}
</page-query>

<script>
export default {
  name: "PostPage",
  metaInfo() {
    return {
      title: this.$page.post.title,
    };
  },
};
</script>

<style>
</style>