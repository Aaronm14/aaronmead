<template>
  <div>
    <Header />
    <div class="container max-w-screen-lg mt-12">
      <h1 class="title text-5xl text-center mb-2">
        Hi, I'm Aaron Mead
      </h1>
      <div class="intro-container flex flex-wrap">
        <div class="w-full md:pr-4 md:w-1/2">
          <div>
            I'm a senior software engineer based in North Carolina.
            I've spent most of my career in the tech industry, largely working at startups.
            Javascript is fun to hate on, but I enjoy writing it and has been a big part of my livelihood for 8 years now.
            Lately I've been working on frontend architecture, specifically with an enterprise Vue.js application.
          </div>
        </div>
        <div class="w-full md:pl-4 md:w-1/2">
          <div>
            When I'm not writing code or working on a side-project, I typically spend my time:
            <ul class="bulleted">
              <li>With my family and friends.</li>
              <li>Being a homebody.</li>
              <li>Watching and consuming content about anything basketball (especially NBA!)</li>
              <li>When I'm not focusing on a project, binge playing some video games (especially <a href="https://na.leagueoflegends.com/en-us/" target="_blank">LEAGUE!</a>)</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="social-links flex items-center justify-start">
        <a
          href="https://www.linkedin.com/in/meadam/"
          target="_blank"
          rel="noopener noreferrer"
          class="btn button-blue mr-1"
        >
          <span class="fa fa-linkedin" /> LinkedIn
        </a>
        <a
          href="https://github.com/aaronm14"
          target="_blank"
          rel="noopener noreferrer"
          class="btn button-gray"
        >
          <span class="fa fa-github" /> GitHub
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
  color: #35495e;
  letter-spacing: 1px;
}

.social-links {
  margin-top: 15px;
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
