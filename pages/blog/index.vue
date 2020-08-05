<template>
  <div>
    <Header />
    <div class="container max-w-screen-lg">
      <h1 class="title text-5xl mb-2">
        Blog Postsy
      </h1>
      <ul>
        <li v-for="article of articles" :key="article.slug">
          <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
            <!-- <img :src="article.img" /> -->
            <article>
              <h2>{{ article.title }}</h2>
              <p>by {{ article.author.name }}</p>
              <p>{{ article.description }}</p>
            </article>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const articles = await $content('articles', params.slug)
      .where({ publish: true })
      .only(['title', 'description', 'img', 'slug', 'author'])
      .sortBy('createdAt', 'asc')
      .fetch()

    return {
      articles
    }
  }
}
</script>
