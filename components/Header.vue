<template>
  <div class="header-wrapper flex justify-center py-5 mb-4">
    <header class="container max-w-screen-lg flex justify-between">
      <div class="header-left">
        <nuxt-link to="/">
          Aaron Mead
        </nuxt-link>
      </div>
      <nav>
        <ul class="flex">
          <li class="mr-6">
            <nuxt-link to="/">
              Home
            </nuxt-link>
          </li>
          <li class="mr-6">
            <nuxt-link to="/work">
              My Work
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/blog">
              Blog
            </nuxt-link>
          </li>
        </ul>
      </nav>
    </header>
    <div
      :class="{'sloth-clicked': slothClicked}"
      class="sloth-container"
    >
      <img
        src="/slothemoji.png"
        @click="slothClicked = !slothClicked"
      >
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      slothClicked: false
    }
  }
}
</script>

<style scoped>
/*
  I don't know why but if styles are added into a component
  instead of globally in tailwind.css, it flashes the old styles before rendering
*/
.header-wrapper {
  background-color: #6A8A74;
  border-bottom: 4px solid #8A6F63;
  position: relative;
}
a {
  @apply text-white text-lg;
  font-weight: bold;
}
a:hover {
  color: #5C778A;
}
nav a {
  @apply underline;
}
nav a.nuxt-link-exact-active {
  @apply no-underline
}
.sloth-container {
  height: 60px;
  position: absolute;
  top: 93%;
  width: 100%;
}
/* TODO: rotate sloth image, make it move on click */
.sloth-container img {
  max-width: 100%;
  max-height: 100%;
  margin: 0 auto;
  cursor: pointer;
}
.sloth-container.sloth-clicked {
    animation: marquee 10s linear infinite;
    animation-delay: -5s; /* To start animation halfway through */
}
@keyframes marquee {
    0% {
        -moz-transform: translateX(calc(-50% - 60px)); /* Must match width of img */
        -webkit-transform: translateX(calc(-50% - 60px));
        transform: translateX(calc(-50% - 60px));
    }
    100% {
        -moz-transform: translateX(calc(50% + 60px));
        -webkit-transform: translateX(calc(50% + 60px));
        transform: translateX(calc(50% + 60px));
    }
}
</style>
