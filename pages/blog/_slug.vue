<template>
  <div>
    <Header />
    <div class="container">
      <article>
        <nav>
          <p class="text-sm font-bold">
            On this page:
          </p>
          <ol>
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
          </ol>
        </nav>
        <pre>Created at: {{ article.createdAt }} </pre>

        <nuxt-content :document="article" />

        <author v-if="article.author" :author="article.author" />
        <prev-next :prev="prev" :next="next" />
      </article>
    </div>
  </div>
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

.nuxt-content p {
  margin-bottom: 20px;
}
</style>
