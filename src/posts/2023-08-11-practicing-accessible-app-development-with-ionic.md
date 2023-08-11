---
title: 'Practicing accessible app development with Ionic'
description: 'I am practicing accessible app development and made a meditation app with the Ionic Framework.'
date: 2023-08-11
---

I have had website development as part of my job responsibilities since 2008 and full time since 2016.

I don't really have professional experience with application development, and it is something that I would like to look at as an option in the future.

Fellow accessibility professional [Todd Libby](https://toddl.dev/) turned me on to the [Ionic Framework](https://ionicframework.com/), which is an accessible application development framework. You can use React, Angular, or Vue.

I have the most experience with React, so I chose that to build my first app. I have worked with React professionally recently to build a custom WordPress Gutenberg block, and I have experimented with creating headless WordPress and Drupal sites with Gatsby and NextJS connecting to a REST or GraphQL API.

I've done little projects off of tutorials such as a to-do list, a pounds-to-kilograms converter, and a weather app that fetches local forecast information from a weather API.

For this project, I wanted to build an app based around a passion of mine: meditation. I built a simple meditation timer app with two-minute, five-minute, and ten-minute timers.

I found a [custom React timer hook](https://www.npmjs.com/package/react-timer-hook) for the timer functionality, and build out the rest using the Ionic framework structure and components.

Ionic allows you to build native mobile apps, but to start off, I'm sticking with making it a web app with PWA functionality (I'm still learning what that means). So for now, I have deployed it to Netlify.

You can [check out the deployed app](https://andy-stitt-meditation-timer.netlify.app/tab1) as well as the [codebase on Github](https://github.com/andystitt829/meditation-timer).

I've tested the basics as far as accessibility, including color contrast and focus visibility. I have yet to dive into accessibility for an app that has text that constantly changes on the screen, such as when you have a timer that is counting down. I have a feeling that I will be learning more about ARIA live regions for this purpose.

I've also learned that TypeScript has a lot of nuances that JavaScript does not. I haven't really learned what those differences are, so I have allowed JavaScript in the tsconfig.json file and changed .ts files to .js to get errors to go away. I will get good at TypeScript someday!