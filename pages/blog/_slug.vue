<template>
  <article>
    <nav>
      <ul>
        <li v-for="link of article.toc" :key="link.id">
          <NuxtLink
            :to="`#${link.id}`"
            :class="{
              'py-2': link.depth === 2,
              'ml-2 pb-2': link.depth === 3
            }"
          >
            {{ link.text }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
    <pre>Created at: {{ article.createdAt }} </pre>

    <nuxt-content :document="article" />

    <author v-if="article.author" :author="article.author" />
    <prev-next :prev="prev" :next="next" />
  </article>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    // Shortcut to view in dev: http://localhost:3000/_content/articles
    const article = await $content('articles', params.slug).fetch()
    const [prev, next] = await $content('articles')
      .only(['title', 'slug'])
      .sortBy('createdAt', 'asc')
      .surround(params.slug)
      .fetch()
    console.log(prev, next)

    return {
      article,
      prev,
      next
    }
  }
}
</script>

<style>
/* Note: Scoped styles don't work with nuxt content */

.icon.icon-link:before {
  display: inline-block;
  font-family: 'FontAwesome';
  content: '\f0c1';
  font-size: 20px;
  padding-right: 5px;
  vertical-align: middle;
  font-weight: normal;
}

.nuxt-content h1 {
  font-weight: bold;
  font-size: 36px;
}
.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
}
</style>
