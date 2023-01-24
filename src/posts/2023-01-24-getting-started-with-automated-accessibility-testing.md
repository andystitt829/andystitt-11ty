---
title: 'Getting started with automated accessibility testing'
description: 'One way to find accessibility errors in the websites that you build is through automated accessibility testing.'
date: 2023-01-24
---

If you're getting started on your accessibility journey as a web developer, one way to find errors in code that you've already written is through automated accessibility testing. There are tools that you can use to automatically detect errors in your code that you can then fix.

You can use these tools to scan sites that you've already built. You're likely to find lots of errors that may take a good amount of time and effort to fix. This is what happens when sites are built and accessibility isn't considered from the beginning. Take note of what you find and show it to your team for prioritizing.

You can also use these tools to scan your work as you're building websites. Just like you would test new components, templates, and pages for cross-browser compatibility, you should also test them for accessibility. Errors found earlier in the process can be fixed more easily.

## My two favorite automated accessibility testing tools

### WebAim WAVE

[WebAim WAVE](https://wave.webaim.org/) is a great starting point for automated accessibility testing. You can put in the URL of a live website to evaluate it, or you can use the Firefox and Chrome extensions to run tests on live sites as well as sites in local and staging environments.

It will show you errors such as insufficient color contrasts, empty links and buttons, missing alternative text on images, empty headings, and form errors. It will also show you alerts that may not necessarily be errors but things are still worth looking into such as redundant alternative text, suspicious link text, and a missing first level heading.

### axe DevTools

[axe DevTools](https://www.deque.com/axe/devtools/) is a Chrome extension made by the company Deque. It shows a lot of the same errors and warnings that WebAim WAVE does, but I find that it's better at showing deeper code level issues. I've found errors with how ARIA is implemented in axe DevTools that WebAim WAVE did not show me.

## Limitations of automated accessibility testing tools

WebAim WAVE, axe DevTools, and other automated tools like it only find a small fraction of accessibility errors. They are no substitute for manual testing, including testing using a keyboard only and with a screen reader.

For example, automated testing tools cannot show that an element on the screen cannot be accessed by your keyboard, or that there's a keyboard trap, or whether or not a skip-link works properly. Only manual testing will show you those things.

Use automated testing tools as your starting point. Use it to start surfacing issues that you can immediately tackle. Make it a habit of doing it whenever you write code in addition to auditing your past work.