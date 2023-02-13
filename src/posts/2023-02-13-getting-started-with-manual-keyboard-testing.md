---
title: 'Getting started with manual keyboard testing'
description: 'One way to find accessibility errors in the websites that you build is through manually testing a web page with your keyboard.'
date: 2023-02-13
---

Many website users don't use a mouse to navigate websites. Instead, they use only their keyboard.

They may have a disability that involves their mobility and motor skills, and moving a mouse steadily enough to navigate a website isn't an option for them. Using the tab and arrow keys on their keyboard works better for them.

It is important that we test the web pages that we build using a keyboard. Here are some things to look out for:

## Make sure all focusable elements are accessible by keyboard

Focusable elements include links, buttons, and form fields. Anything that you can click on or click into with a mouse, you should be able to access it using the tab or arrow keys on your computer.

As you tab through elements, make sure you're moving forwards and backwards. Holding down the shift key while pressing tab will allow you to move backwards through focusable elements.

## Make sure there are no keyboard traps

If a page that you're testing only has links, then you're unlikely to find a keyboard trap. If a page you're testing has more complex elements such as form fields or modal windows, you might find a keyboard trap.

A keyboard trap is a part of a website where no matter how many times you tab forwards and backwards, you can't get out of a specific section abd back to other elements of the website.

It's called a keyboard trap because keyboard focus becomes trapped in that section of the website. Make sure that the websites you develop don't contain any keyboard traps by testing for them.

## Make sure that all focusable elements have a visible focus outline

As you tab through different elements on the web page that you're testing, look to see if you know which focusable element is receiving focus at that time. Does it change color? Does it have an outline around it? Are words underlined?

In order for content to be keyboard accessible, you have to know where you are and what is receiving keyboard focus at any given time. If you don't know where you are, then you can write CSS styles for the elements that are not receiving focus, such as putting a visible outline around the element.

## Make sure to keyboard test mobile screen sizes

Many users have keyboards for their mobile devices if their disabilities doesn't allow for them to scroll, swipe, and tap with their fingers.

As far as I know, if you don't have a keyboard for a mobile device, you can adjust the screen width in your desktop browser so the mobile version of the site appears and test with your computer keyboard.

## Make keyboard testing a part of your testing toolbox

[Automated accessibility testing](/blog/getting-started-with-automated-accessibility-testing/) can quickly help pick up errors that are easily detectable. Manual testing detects errors that automated testing cannot. Keyboard testing is a key part of manual testing. It will help you make websites and applications that are more accessible if you keyboard test the code that you write as you write it.