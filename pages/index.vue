<template>
  <div>
    <Header />
    <div class="container">
      <h1 class="title">
        aaronmead
      </h1>
      <div class="links">
        <a
          href="https://www.linkedin.com/in/meadam/"
          target="_blank"
          rel="noopener noreferrer"
          class="btn button-blue"
        >
          LinkedIn
        </a>
        <a
          href="https://github.com/aaronm14"
          target="_blank"
          rel="noopener noreferrer"
          class="btn button-gray"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
/* .main-content {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
} */

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.btn {
  @apply font-bold py-2 px-4 rounded;
}
.button-blue {
  @apply bg-blue-500 text-white;
}
.button-blue:hover {
  @apply bg-blue-700;
}
.button-gray {
  @apply bg-gray-500 text-white;
}
.button-gray:hover {
  @apply bg-gray-700;
}
</style>
