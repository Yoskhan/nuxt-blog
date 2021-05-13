<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news.</h1>
    </section>
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "~/components/Posts/PostList";
export default {
  middleware: "log",
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts;
    },
  },
  // data() {
  //   return {};
  // },
  components: {
    PostList,
  },
};
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url("~assets/images/main-page-background.jpg");
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: white;
  background-color: rgba(0, 0, 0, 0.7);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}
</style>