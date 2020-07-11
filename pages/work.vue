<template>
  <div>
    <Header />
    <div class="container">
      <h1 class="title">
        My Work
      </h1>
      <p>Visualize in a timeline? Asc or Desc order?</p>
      <p>
        Maybe each heading could be a dropdown or toggle with a tdlr;
        In the style of https://nbadraft.theringer.com/ (Skim Peruse Deep Dive)
      </p>
      <!-- Find a format for each experience, maybe biggest takeaway learning from job -->
      <h2>Allstacks</h2>
      <p>Screenshots of the app</p>
      <p>How I joined, state of the company & codebase at the time</p>
      <p>Starting as only FE engineer, prioritizing legacy conversions, making decisions with no direct peers</p>
      <!--
        Standards to start checking code by
        Accessibility (including semantic html)
        Minimum responsiveness level (TBD)
        Allstacks component consistencies / styleguide
        Adding typescript as we go (whatever reqs we come up with)
      -->
      <!--
        When we hired 2nd FE engineer, I/we came up with this list
        // show which ones we've done, each could have a paragraph
        // with how we went about it and how helpeful its been
        Linting
        Component Library
        Testing
        SPA
        Typescript
        Vuex
        Performance - API calls & Bundle size reduction
        Responsive
        Rip out bootstrap
        Error Reporting / Handling
        SPA
       -->
      <h2>Full Time Independent</h2>
      <p>Ready for change of pace of heavy hours, how I transitioned freelance work to support</p>
      <p>Learnings / failures</p>
      <p>Bball app w/ context and screenshots</p>
      <p>CM app w/ context/screenshots and publish code to Github</p>
      <p>How coworking turned into Allstacks</p>

      <h2>K4Connect</h2>
      <p>How I found out about the company, joining when there were only 4 other FTEs (and Scott being out)</p>
      <p>Why I left last job, my experience leading up to this (MEAN stack on side was it)</p>
      <p>My work first year or two, having no other engineers besides CTO to ask questions</p>
      <p>Projects + screenshots + learnings for each</p>
      <ul>
        <li>Enyo.js app</li>
        <li>Learning about bluetooth, zwave, etc. (tested various devices, some very low level stuff)</li>
        <li>Building on structure from CTO for MEAN stack app (dashboard)</li>
        <li>Building operations tool prototype (stunk, rebuilt with angular 1.6, which then was rebuilt with ext.js)</li>
        <li>Resident app 2.0 with angular (built features that were whole standalone biz like video chat, events, msging)</li>
      </ul>
      <p>Quitting in good faith with long notice, being offered to stick around with changes</p>
      <p>Learnings from being in a testing role</p>

      <h2>Coffee Crate</h2>
      <p>Working with friends, how idea happened</p>
      <p>Managing time working on this on the side</p>
      <p>Stories of appearing in news, no website visitors, selling biz</p>
      <p>Getting to know CJ team leading to freelancing work and value of doing good work</p>

      <h2>Kadro</h2>
      <p>Starting off in support, first job</p>
      <p>Custom ecommerce platform, writing html in the system</p>
      <p>Early responsive dev, supporting back to IE7</p>
      <p>Magento, learning JS, having to take on bad projects, learning value of profit / scope creep</p>
      <p>Culture of company amazing, but not scratching itch to learn more tech or focus on a product</p>

      <h2>Orasi</h2>
      <p>Fast growth, then slowing down</p>
      <p>Ended up being great the work was mind numbingly boring, huge desire to learn to code</p>
      <p>But got professional experience, mainly took because relationship getting more serious</p>

      <h2>Coaching?</h2>

      <h2>If timeline is h2, then this h2 could be general career learnings, side projects etc</h2>

      <h2>Career principles?</h2>
      <p>Balance (work/life, new features/refactor, learning new tools etc), always do your best work & take ownership, be T shaped, follow the founders</p>
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
</style>
