<template>
  <div class="header-wrapper flex justify-center py-5 mb-4">
    <header class="container flex justify-between">
      <div class="header-left">
        <a href="/">Aaron Mead</a>
      </div>
      <div class="sloth-container">
        <img src="/slothemoji.png">
      </div>
      <nav>
        <ul class="flex">
          <li class="mr-6">
            <a href="/#about">About</a>
          </li>
          <li class="mr-6">
            <a href="/work">Work</a>
          </li>
          <li>
            <a href="/blog">Blog</a>
          </li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<style>
/*
  I don't know why but if styles are added into a component
  instead of globally in tailwind.css, it flashes the old styles before rendering
*/
.header-wrapper {
  background-color: #6A8A74;
  border-bottom: 4px solid #8A6F63;
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
.sloth-container {
  height: 60px;
  position: absolute;
  left: 50%;
  transform: translate(-50%, 64%);
}
/* TODO: rotate sloth image, make it move on click */
.sloth-container img {
  max-width: 100%;
  max-height: 100%;
}
</style>
