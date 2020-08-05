---
title: Thinking In vue
author: 
    name: Aaron
    bio: Aaron's bio
		image: https://source.unsplash.com/random/?person
publish: false
---

## Thinking in Vue

The great thing about Vue is how flexible it is, but it also means people bring concepts and mental models from outdated ways of doing things.  That's actually okay, and makes Vue an easy transition, but can lead to: inconsistencies in code between devs, more bug-prone code, and not taking advantage of the performance improvements Vue provides.

## Reactive Javscript
In our own codebase I have seen object-oriented, functional, and now "reactive" javascript.

Object-oriented code was probably written by those with more backend experience.  It fits with the mental model they have when thinking about component architecture.  For example, each chart type inherits from a base chart, and overrides the specific methods when it needs to do something differently.  This has some advantages in use cases with clear inerhitance based examples, but doesn't match any patterns used by modern javascript applications.

Functional javascript is supposed to be building functionality by chaining together of "pure functions", avoiding shared state, mutable data, and side-effects.  In practice, it is rare all of those goals are met, and sometimes that is okay.  So when a button is clicked, someone will explicitly say `this.loading = true; this.loadData(); this.loading = false();` This has side effects but it gets the job done and is easy to reason about what is going on.

But what about when the button also has to manipulate the DOM and update another part of the application with the new data that was loaded in, or that button also needs to track errors?  That complexity quickly grows and it becomes easy to leave off a `this.loading = false` which can get your application stuck.

With Reactive programming, instead of saying when this happens, do x, y, and z, you can say x depends on y which depends on z.  So any time z is updated, y and x automatically updated.  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy With Proxies now in Javascript, it has first class support for this model, which Vue.js already made part of its core offering

Of course, there are always opportunies to screw things up regardless of what pattern is use.  The biggest thing is consistency and then picking the best pattern for the tools you are using and the app you are creating.


https://www.sitepoint.com/introduction-functional-javascript/
https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0