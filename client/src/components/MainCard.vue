<template>
  <div class="card mb-3 p-0 mx-0">
    <img
      class="card-img-top"
      :src="article.image"
      alt="Card image cap"
      style="height: 300px; object-fit: cover;"
    />
    <div class="card-body">
      <h5 class="card-title">{{article.title}}</h5>
      <div v-html="article.content"></div>
      <p class="card-text">
        <small class="text-muted">By {{article.userId.firstName}} {{article.userId.lastName}}</small><br>
        <small class="text-muted">~Last updated 3 mins ago</small>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainCard",
  props: ["article"]
};
</script>

<style scoped>
</style>