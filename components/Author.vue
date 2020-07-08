<template>
  <div>
    <NuxtLink :to="`/blog/author/${author.name}`">
      <div
        :style="{'background-image': `url(${author.image})`}"
        class="author-img-container"
      />
      <div>
        <h4>Author</h4>
        <p>{{ author.name }}</p>
        <p>{{ author.bio }}</p>
      </div>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>
.author-img-container {
  width:  60px;
  height: 60px;
  border-radius: 50%;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
