<template>
  <div>
    <Header />
    <div class="container my-work-container">
      <h1 class="title">
        My Work
      </h1>
      <p>Visualize in a timeline? Asc or Desc order?</p>
      <p>
        Maybe each heading could be a dropdown or toggle with a tdlr;
        In the style of https://nbadraft.theringer.com/ (Skim Peruse Deep Dive)
      </p>
      <!-- Find a format for each experience, maybe biggest takeaway learning from job -->
      <work-item
        :screenshot="imagePaths.allstacks"
        title="Allstacks"
        title-url="http://allstacks.com/"
      >
        <template v-slot:intro>
          <p>
            Initially I joined Allstacks as a consultant, I quickly found enjoying the small team of ~5 full time employees and the culture they created, so joined full time after just two weeks.

            The codebase was a Django app that recently started sprinkling in Vue.js, so I led efforts to gradually convert the frontend to modern Vue best practices.
          </p>
          <p>
            After being the only FE engineer for about a year, we brought in two FE engineers.  Around that time I was able to take the time take inventory of best practices already implemented and where we still needed to be.  So far, we have successfully used an incremental improvement strategy to implement:
          </p>
        </template>
        <template v-slot:description>
          <ul>
            <li><strong>Single File Vue Components:</strong> Most existing code, and all new code is compiled via webpack so we can leverage SFCs.</li>
            <li><strong>Standard ESLint configs:</strong> All autofixable problems were fixed, and now practice the "leave it better than we found it" for everything else.</li>
            <li><strong>A Component Library:</strong> Storybook to document our base components built on top of Vuetify components.</li>
            <li><strong>Unit Testing:</strong> Gradually adding Jest unit tests, first on new code, and gradually to older code without tests.</li>
            <li><strong>Cypress:</strong> Got Cypress running against our Django-templated app, with a goal of replacing flaky Selenium tests.</li>
            <li><strong>Typescript:</strong> New code gets types where they can be the most beneficial, but we aren't concerned about getting to 100% conversion.</li>
            <li><strong>Vuex Standards:</strong> Shored up old Vuex code that didn't fit with how we want to approach our stores, and created standards for building new ones.</li>
            <li><strong>Performance:</strong> The biggest wins were condensing API calls in some cases, then gradually reducing package sizes with better 3rd party library management.</li>
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
        </template>
      </work-item>
      <work-item
        :screenshot="imagePaths.newAcorn"
        title="Full Time Independent"
      >
        <template v-slot:intro>
          <p>A desire to have a more flexible lifestyle for my family led me down a familiar entrepreneurial path.  I had done good work on Cratejoy's platform and their team took notice and referred people that needed website help to me.  It seemed I had enough work to do consulting work part time then invest in building my own products that could eventually replace my consulting income.</p>
          <p>Does that last sentence sound familiar?  Its because nearly every engineer has the same thought process.  Ironically, when meeting folks in the area I could learn from, my future employer told me they were in my shoes and ultimately discovered they ended up not doing either thing well.  My experience didn't prove to be too different. But I did work I was proud of:</p>
        </template>
        <template v-slot:description>
          <ul>
            <li><strong>Consulting:</strong> Cratejoy websites and integrations were my bread and butter, but the most fun work was a few projects I had with local startups. One of which <a href="https://github.com/acunniffe/optic-vscode-plugin" target="_blank">open sourced my work</a> and later got into Y Combinator!  Additionally one of the startups I worked with for two weeks ended up convincing me to join them full time.</li>
            <li><strong>Scorekeeping App</strong> My first product-focused project was partnering with a company that was exploring building an ancillary tool.  It was my first foray into Angular 2+ and Typescript, which I found to be really helpful after the initial learning curve.</li>
            <li><strong>Campus Minister App:</strong> I worked with a friend on a tool for college campus ministers to broadcast text messages to their students.  It worked well and was used on a regular basis for a couple years by someone at a state university here.  The coolest part about the app technically was that it was all severless thanks to Firebase and Google Cloud Functions.</li>
          </ul>
        </template>
      </work-item>

      <work-item
        :screenshot="imagePaths.k4Connect"
        title="K4Connect"
        title-url="http://k4connect.com/"
      >
        <template v-slot:intro>
          <p>It felt like a big deal in a medium sized city when a founder who was the CEO of a company that ultimately became the finger print scanner in the iPhone was starting a new company.  I got to meet some of the team at a node.js meetup and luckily for me, I was offered a job when the CTO recognized my experience working on side projects and entrepreneurial spirit.</p>
          <p>During my 3 years at K4Connect, we grew from 5 to ~40 some full time employees. I was learning <em>a ton</em> and having fun while I was doing it. I worked on all sorts of projects and technologies:</p>
        </template>
        <template v-slot:description>
          <ul class="bulleted">
            <li><strong>Enyo.js:</strong> When I first joined, the first version of the resident-facing app was built on Enyo.js.  Luckily we re-wrote it in Angular not long after I joined.</li>
            <li><strong>MongoDB, Angular.js, and Node.js:</strong> Early versions of a dashboard application were built using the MEAN stack, including socket.io for real time features.</li>
            <li><strong>IoT:</strong> Our controller that interfaced with the hardware we installed used in node.js bridges for devices using bluetooth, zwave, etc.</li>
            <li>We had single features in a few of these apps that were whole businesses at other companies.  Photo libraries, real time video chat, event management, messaging, smart home controls, and more.</li>
          </ul>
        </template>
      </work-item>

      <work-item
        :screenshot="imagePaths.coffeeCrate"
        title="Coffee Crate"
        title-url="https://web.archive.org/web/20150716073316/http://www.coffeecrate.co/"
      >
        <template v-slot:description>
          <p>I started a coffee subscription box with a couple of friends during our nights and weekends and quickly grew it to profitability.  It was my full focus outside of my day job and social life.  It was a fun challenge that proved hard work isn't nearly as hard when that work is also fun.</p>
          <p>Eventually my next job opportunity felt too good to pass on, and with the extra hours that came long with it, we decided to sell the business 10 months in.  It was bittersweet, but the right move in retrospect.</p>
          <p>Throughout this time I noted stories of early platform adopters because we leveraged a new subscription box platform called Cratejoy.  I made sure to do good work on the platform and be helpful to the Cratejoy team while we benefited from their tool.  This proved to be a good move in a few years... </p>
        </template>
      </work-item>

      <work-item
        :screenshot="imagePaths.kadro"
        title="Kadro"
        title-url="http://kadro.com/"
      >
        <template v-slot:intro>
          <p>Each job I've gotten has been a big step forward in my career in some way or another, but perhaps this was the biggest one.  I was getting paid to write code full time, and I was learning the ins and outs of technical consulting.  It was one of the best cultures I've been a part of to boot, which was especially important as I had just gotten married.</p>
          <p>Perhaps even more important than the technical learnings was getting a peak behind the curtains at the business side of things.  Developers at Kadro fortunately got to be hands on in scoping out projects and seeing how profitable they were.</p>
        </template>
        <template v-slot:description>
          <ul class="bulleted">
            <li><strong>SQL:</strong> My first role here was doing technical support on a proprietary ecommerce platform.  I wrote a lot of SQL queries to update data or fix orders for clients.</li>
            <li><strong>Web Development:</strong> Later I became the only fully focused frontend developer.  I churned through a lot of PSD designs, converting them to responsive HTML/CSS back when mobile traffic was still sub 10% on most websites.  Oh and sites had to work on IE7...</li>
            <li><strong>Magento:</strong> Along with just a couple others, I began focusing on Magento projects and earned one of the early Magento Frontend certifications.  I also got more experience with PHP, unix, and more advanced Javascript.</li>
          </ul>
        </template>
      </work-item>

      <work-item
        title="Orasi"
        title-url="https://www.orasi.com/"
      >
        <template v-slot:intro>
          <p>My first full time job out of college was making $11/hr at an over-ambitious software testing company that was initially growing like hot cakes, only to realize they bit off more than they could chew.</p>
          <p>The main benefits I got here were simply getting experience on my resume and doing mind numbingly boring work.  The latter is actually great fuel for learning new skills on the side.</p>
          <p>This is where I got more serious about focusing on programming since it was all I wanted to do while I was manually testing apps made by Disney.</p>
        </template>
      </work-item>

      <!-- <h2>Coaching?</h2>

      <h2>If timeline is h2, then this h2 could be general career learnings, side projects etc</h2>

      <h2>Career principles?</h2>
      <p>Balance (work/life, new features/refactor, learning new tools etc), always do your best work & take ownership, be T shaped, follow the founders</p> -->
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      imagePaths: {
        allstacks: '/milestone-report.png',
        newAcorn: '/cm-app.png',
        k4Connect: '/community-app.jpg',
        coffeeCrate: '/coffee-crate-box.png',
        kadro: '/reeds.jpg'
      },
      videoPaths: {
        newAcorn: '/transition-flip.webm'
      }
    }
  }
}
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

p {
  @apply mb-4
}
.my-work-container a {
  @apply underline
}

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

.portfolio-img-container {
  width: 100%;
  height: 260px;
  background-repeat: no-repeat;
  background-size: contain;
}
/*
.job-content-images {
  @apply pr-4 w-1/1
}
.job-content-text {
  @apply pr-4 w-1/1
}
/* Medium (md) */
/*@media (min-width: 768px) {
  .job-content-images {
    @apply w-1/4
  }
  .job-content-text {
    @apply w-3/4
  }
}

@responsive {
  .bg-gradient-brand {
    background-image: linear-gradient(blue, green);
  }
} */

</style>
