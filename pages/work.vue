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
      <p>The entrepreneurial itch I experienced when I started working on Coffee Crate made its return on top of wanting even more flexibility with my lifestyle.  So, I began gradually making steps to ensure I could get a foundation of consulting work off the ground to pay the bills.  Alluding back to my time working on Cratejoy, I had made some good connections internally on top of doing good work.  So much so that they were referring me clients.  I had niched into this platform and was able to build a steady enough amount of work that I could do consulting work part time and not make terribly worse money than I was making full time.  The goal was to roughly split my time trying to build my own products that could eventually replace my consulting income.</p>
      <p>Does that last sentence sound familiar?  Its because nearly every engineer has the same thought process.  Ironically, when meeting folks in the area I could learn from, my future employer told me they were in my shoes and ultimately discovered they ended up not doing either thing well.  My experience didn't prove to be too different.  I was stressed because I couldn't devote the time my projects deserved.  To make matters worse I was exploring two products at once.</p>
      <p>Luckily the learnings I mentioned at Kadro really proved to be fruitful here.  I never had any major issues on any client projects, I avoided any major scope creep and almost every project turned out profitable even after factoring non-billable time spent.</p>
      <p>Here was what most of my time was spent on:</p>
      <ul>
        <li>My first product focused project was partnering with a company that was exploring building an ancillary tool they didn't have time to build themselves.  It was my first foray into Angular X and Typescript, which I found to be really helpful after the initial learning curve.</li>
        <li>At the same time, I was working with a friend on a tool for college campus ministers to broadcast text messages to their students.  It worked really well, and was used on a regular basis for a couple years by someone at a state university here.  The coolest part about the app was that it was all severless.  We leveraged Firebase and Google Cloud Functions to keep the costs at virtually 0.  The most expensive piece was certainly sending SMS, but <a href="https://www.bandwidth.com/messaging/">Bandwidth SMS</a> gradually turned into a more enterprise focused app as they IPO'd.  This project ultimately hit a point where we couldn't achieve multi-tenancy without starting over on a few things, and as the project wasn't my full focus, it just stayed in a limbo state.</li>
        <li>Consulting wise, Cratejoy websites and integrations were my bread and butter, but the most fun work was a few projects I had with local startups, one of which <a href="https://github.com/acunniffe/optic-vscode-plugin" target="_blank">open sourced my work</a> and later got into Y Combinator!  Additionally one of the startups I worked with for two weeks ended up convincing me to join them full time.</li>
      </ul>

      <h2>K4Connect</h2>
      <p>Knowing that I may want to start my own company or join a startup one day, I stayed involved with the tech ecosystem in my area.  I had heard K4Connect's CEO had previously taken his previous company public before selling to Apple, and who's technology would become the fingerprint scanner on the iPhone.  This felt like a big deal for a medium sized city.  I later went to a node.js meetup where the CTO was giving a talk where I honestly felt like the content was over my head.  But I got to meet some of the team and turned out they had an opening for a full stack engineer.  Luckily for me, the CTO recognized my experience working on side projects and entrepreneurial spirit and ultimately gave me the opportunity to join the company.</p>
      <p>To say that it was like drinking through a firehouse would be an understatement starting out here, and I was on a roller coaster of feeling like I could never figure out certain problems and just having a flat out blast.  The early days especially were an incredible experience getting to work in the downtown office, initially with just 4 other full time employees.</p>
      <p>Up until this point I pretty much only done real backend or javascript framework programming on the side, and I certainly had no experience interfacing with Bluetooth and Z-Wave hardware.  The only other full time engineer was the CTO, and he was spending less and less time writing code.  Learning in that environment certainly had its pros and cons, but the pros far outweighed the cons.  I was learning <em>a ton</em> and having fun while I was doing it, other than the frequent feelings of being a fraud.</p>
      <p>During my 3 years at K4Connect, we grew to ~40 some full time employees, and I worked on all sorts of projects:</p>
      <ul>
        <li><strong>Enyo.js</strong> When I first joined, the first version of the resident-facing app was built on Enyo.js.</li>
        <li>Our controller that interfaced with the hardware we installed was written mostly in node.js to build bridges for bluetooth, zwave, etc.</li>
        <li><strong>MongoDB, Angular.js, and Node.js</strong>Our early versions of a dashboard application was built using the MEAN stack including socket.io for some real time features.</li>
        <li>Our aesident app was later rebuilt Angular.js and a slew of other technologies.  We had single features that were whole businesses at other companies.  Photo libraries, real time video chat, event management, messaging, smart home controls, and more.</li>
      </ul>
      <p>The long hours on top of being married to someone working night shift gradually burned me out.  I had initially quit with several months notice so the company had ample time to find a replacement, with the goal being to find do freelance work to pay the bills.  Fortunately they worked with me to let me move to a less critical role and do some development and some testing, in exchange for working less hours and have some remote flexibility.</p>

      <h2>
        <a href="https://web.archive.org/web/20150716073316/http://www.coffeecrate.co/" target="blank">Coffee Crate</a>
      </h2>
      <p>I had originally learned how to code so I could start a tech company.  As my learning gradually plateued, the entrepreneurial itch kicked in and I started a coffee subscription box with a couple of friends during nights and weekends.  I learned building a business with your friends is one of the most fun things you can do.</p>
      <p>Looking back, I'm still not entirely sure how I made the time for it other than it was my full focus outside of my day job and social life.  It was a fun challenge that proved hard work isn't nearly as hard when that work is also fun.</p>
      <p>Eventually my next job opportunity felt too good to pass on, and with the extra hours that came long with it, we decided to sell the business 10 months in.  It was bittersweet, but the right move in retrospect.</p>
      <p>Throughout this time I was thinking about stories of early platform adopters because we leveraged a new subscription box platform called Cratejoy while it was in beta to quickly start a profitable business.  I made sure to do good work on the platform and be helpful to the Cratejoy team while we benefited from their tool.  This proved to be a good move in a few years... </p>

      <h2>Kadro</h2>
      <p>Each job I've gotten has been a big step forward in my career in some way or another, but perhaps this was the biggest one.  I was getting paid to write code full time, and I was learning the ins and outs of technical consulting.  It was one of the best cultures I've been a part of to boot, which was especially important as I had just gotten married.</p>
      <p>My first role here was doing technical support on a proprietary ecommerce platform.  It mostly involved writing a lot of SQL queries to update data or fix orders.  Perhaps even more importantly it gave me a lot of experience working directly with our customers.</p>
      <p>As time went on my role evolved into being the only fully focused frontend developer.  I churned through a lot of PSD designs, converting them to responsive HTML/CSS back when mobile traffic was still sub 10% on most websites.  Oh and it had to work on IE7...</p>
      <p>During that time I along with a few others in the company began focusing on Magento projects and I earned one of the early Magento Frontend certifications.  It was here that I got more experience with PHP, unix, and more advanced Javascript.</p>
      <p>Perhaps even more important than the technical learnings was getting a peak behind the curtains at the business side of things.  Developers at Kadro fortunately got to be hands on in scoping out projects and seeing how profitable they were.  This surely had tens of thousands of dollars worth of value to me as I took on freelancing and consulting later on.</p>

      <h2>Orasi</h2>
      <!-- <p>My first full time job out of college was making $11/hr on a 6 month contract-to-hire gig doing manual software testing.  Orasi was hiring a lot of recent college grads, there was a new cohort coming in every week for a time.  They had stereotypical office goodies: open office floor plan, nerf gun fights, snacks in the kitchen and a Wii.  I later realized the "perks" and promise of an eventual $80k+ salary just mostly a ploy to convince impressionable and eager recent grads to do mind numbing work.  On the plus side, disliking your job is great fuel for picking up new skills</p> -->
      <p>My first full time job out of school was making $11/hr at an over-ambitious software testing company that was initially growing like hot cakes, only to realize they bit off more than they could chew.  The main benefits here were simply getting experience on my resume and doing mind numbingly boring work.  The latter is actually great fuel for learning new skills on the side.  This is where I got more serious about focusing on programming since it was all I wanted to do while I was manually testing apps made by Disney.</p>

      <!-- <h2>Coaching?</h2>

      <h2>If timeline is h2, then this h2 could be general career learnings, side projects etc</h2>

      <h2>Career principles?</h2>
      <p>Balance (work/life, new features/refactor, learning new tools etc), always do your best work & take ownership, be T shaped, follow the founders</p> -->
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
</style>
