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
      <p>
        Initially I joined Allstacks as a consultant with the offer to join full time if I enjoyed it.  I quickly found enjoying the small team of ~5 full time employees and the culture they created, so joined after just two weeks.

        I had the opportunity to act as the de facto frontend lead, as the other couple engineers were backend focused.  It was a typical Django application that recently started sprinkling in Vue.js on top of the existing jQuery + Bootstrap code.

        Our tool was built for engineering managers and was starting to find some solid traction when I joined.
      </p>
      <p>
        While I had been the only frontend focused engineer before, I was now being entrusted with choosing best practices and responsible for the direction of this piece of the codebase.

        Since this was a startup, I also had to balance the needs of the frontend code with the needs of the business and stakeholders.  This meant I didn't have free reign to just toss all legacy code and slowly rebuild it using modern Vue best practices.

        The strategy we settled on could be boiled down to two main principles: leave it better than where you found it and better to improve it incrementally than not work on it at all.  I am always asked: "what is the incremental approach to this?"

        So instead of refactoring everything in one fell swoop, we'd often wait until tackling a specific feature on a page to upgrade it to "modern Vue."  Specifically this looked like updating Django templates + jQuery or Vue.js injected like jQuery to using single file vue components and APIs where possible to render data.

        This has been a fun challenge for me, especially early on when I was the only dedicated frontend engineer.  It forced me to be decisive rather than deliberate back and forth with a group and rely on them or someone else for the final choice.
      </p>
      <p>
        After being the only FE engineer for about a year, we brough in two FE engineers.  I was able to take the time take inventory of all the practices we wanted to start implementing.  So far, we have successfully added in:
      </p>
      <ul>
        <li><strong>Standard ESLint configs</strong> & linted most of the frontend code.  The incremental approach here was to fix all autofixable problems, then leave it better than we left it as time went</li>
        <li><strong>A Component Library</strong> - We went with Storybook to document our base components built on top of Vuetify components.  This allows both engineers and designers to at a glance see variations of components like buttons</li>
        <li><strong>Unit Testing</strong> - We have been gradually improving our unit test coverage using Jest, first on new code, and gradually to older code without tests.  These are mostly for Vue computed properties and methods and Vuex actions and mutations</li>
        <li><strong>Typescript</strong> - The great thing about Typescript is it can be added incrementally, which is exactly what we've done.  New code gets types where they can be the most beneficial, we aren't concerned about getting to 100% conversion</li>
        <li><strong>Vuex Style Guide</strong> - My coworker made a great Vuex style guide that we use as a standard for old and new code alike.  We were able to invest the time to shoring up old Vuex code that didn't fit with how we want to approach our stores</li>
        <li><strong>Performance</strong> - I made some significant strides, though there is a long way to go.  The biggest wins were condensing API calls in some cases, then greatly reducing package sizes by moving shared libraries and finding modern substitutes for packages we used sparingly</li>
      </ul>
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
