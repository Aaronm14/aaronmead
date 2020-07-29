<template>
  <article>
    <h2 :id="`${title}-heading`" class="my-4">
      <a
        :href="titleUrl || `#${title}-heading`"
        :target="titleUrl ? '_blank' : ''"
      >
        {{ title }}
      </a>
    </h2>

    <slot name="intro" />

    <div
      v-if="screenshot"
      class="job-content flex flex-wrap"
    >
      <div class="job-content-images w-full md:pr-2 md:w-1/3">
        <div
          :style="{'background-image': `url(${screenshot})`}"
          class="portfolio-img-container"
        />
      </div>

      <div class="job-content-text w-full md:pl-2 md:w-2/3">
        <slot name="description" />
      </div>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    titleUrl: {
      type: String,
      required: false,
      default: ''
    },
    screenshot: {
      type: String,
      required: false,
      default: ''
    }
  }
}
</script>
