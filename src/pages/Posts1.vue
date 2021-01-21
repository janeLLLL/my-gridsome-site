<template>
  <Layout>
    <div>
      <h1>Post1</h1>
      <ul v-for="edge in $page.posts.edges" :key="edge.node.id">
        <g-link :to="edge.node.path">{{ edge.node.title }}</g-link>
      </ul>
    </div>
  </Layout>
</template>

<page-query>
query {
  posts: allPost {
    edges {
      node {
        id
        title
        path
      }
    }
  }
}
</page-query>

<script>
export default {
  name: "Post1",
  data() {
    return {};
  },
};
</script>

<style>
</style>