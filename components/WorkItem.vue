<template>
  <article>
    <h2>{{ title }}</h2>
    <slot name="intro" />
    <div class="job-content flex flex-wrap">
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
    screenshot: {
      type: String,
      required: true
    }
  }
}
</script>
