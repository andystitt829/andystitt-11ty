---
title: 'Six common accessibility errors found on websites'
description: 'Learn about six common accessibility errors that are found on websites and how to fix them.'
date: 2023-06-07
---

[The WebAIM Million report](https://webaim.org/projects/million/) scans the homepages of the top one million websites and reports its findings regarding accessibility errors. The six most common errors in these reports have been the same for the last five years that the report has been conducted.

These errors are easier to fix than other errors where you are dealing with more complex code and design patterns. This is part of the low-hanging fruit that you can target to make major progress when making accessibility fixes on existing sites and what to pay attention to when starting new projects.

Six common website accessibility errors are:

## Low contrast text

When people build websites without accessibility in mind, they don't test the contrast of the font color against the background color to make sure that the contrast ratio is high enough. There are lots of color contrast checkers you can use. I use the [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/).

This checker will let you know if you've passed or failed and at what level according to the Web Content Accessibility Guidelines, otherwise known as WCAG. At minimum, you need the colors to pass at the AA level. The AA level has its own minimum contrast ratio requirements, and the contrast ratio at the AAA level is even higher.

## Missing alternative text for images

When building accessible websites, the goal is information parity. Whatever information a sighted user can see on a website should also be able to be accessed by a blind or low-vision user that uses a screen reader.

Whatever a sighted user sees in an image should be described in that image's alternative text. Try not to be under-descriptive or over-descriptive. Just describe what's in the image; what you think people would want to know about it.

There are lots of schools of thought about how alternative text should be written, but the most important starting point for you is to put in the effort to begin with. You will get better at it over time.

There are images that are used strictly for decoration called decorative images, and these images don't need alternative text. However, I've found that so many people forget or don't know to put alternative text in any images at all. So, most images that you come across will need alternative text.

## Empty links

Most of the time, empty links occur when, in the HTML, you wrap an icon in `<a>` tags and there's no accompanying text to identify what the link is going to. 

For example, this can happen with Font Awesome icons. Let's say you want to link to your Facebook page, and you use the Font Awesome icon to do it. This would be the HTML:

`<a href="https://facebook.com/your-facebook-page-URL"><i class="fa-brands fa-square-facebook"></i></a>`

This would trigger an accessibility error since there is no text describing what the link goes to.

There are a number of ways that you can fix this. You can add a title attribute to the `<a>` tag like this:

`<a href="https://facebook.com/your-facebook-page-URL" title="My Facebook page"><i class="fa-brands fa-square-facebook"></i></a>`

You can add an aria-label attribute to the `<a>` tag like this:

`<a href="https://facebook.com/your-facebook-page-URL" aria-label="My Facebook page"><i class="fa-brands fa-square-facebook"></i></a>`

Finally, you can add text that is invisible on the front-end of the website but visible to screen readers and other assistive technologies. This is commonly referred to as "screen reader-only text". For example, if you use the Bootstrap framework, it has a CSS class called `.sr-only` that you can apply like this:

`<a href="https://facebook.com/your-facebook-page-URL"><span class="sr-only">My Facebook page</span><i class="fa-brands fa-square-facebook"></i></a>`

One practice that I use at work is to make sure that the Facebook icon is hidden from screen readers and other assistive technologies by adding the `aria-hidden="true"` attribute. The whole piece of code looks like this:

`<a href="https://facebook.com/your-facebook-page-URL"><span class="sr-only">My Facebook page</span><i class="fa-brands fa-square-facebook" aria-hidden="true"></i></a>`

There could be other ways of generating empty links, but this is the most common one that I see and how to fix it.

## Missing form input labels

Every time you put a form input box on a website, you need to give it a label. The easiest way to do this is to use the `<label>` tag. Here's an example:

`<label for="first-name">First Name</label><input type="text" id="first-name">`

Make sure that the `<label>` "for" attribute matches the `<input>` "id" attribute. That's the only way to associate the label with the input box programmatically so that assistive technologies are able to announce the input box with the correct label.

Please note that the "placeholder" attribute in the `<input>` tag is not a replacement for a `<label>`. Though the placeholder text is visible to sighted users, as soon as they click their mouse or tab into the field using their keyboard and start typing, the placeholder text goes away. There needs to be a persistent label for the input field that doesn't disappear when the user takes any kind of action.

## Empty buttons

This is very similar to empty links. Most of the time you will see buttons with icons and no other text get flagged by accessibility scanners as empty buttons. Just like with the `<a>` tag, you can use the "title" or "aria-label" attributes with the `<button>` tag or add screen reader-only text between `<span>` tags with the appropriate CSS class, such as `.sr-only` in Bootstrap.

## Missing document language

The `<html>` tag at the top of the document needs to have a "lang" attribute. If your website is in English, then the full code would be `<html lang="en">`. Assistive technologies need to know what language to read the document in.

You can access a full list of language codes from the [Internet Assigned Numbers Authority Language Subtag Registry](https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry).

If you ever have a portion of a web page in a different language than the rest of it, then you can add the "lang" attribute to that portion of content only. For example, if you have a paragraph of text in Spanish on an otherwise English language page, then you can have `<p lang="es">` as the beginning paragraph tag.

For fun, create a web page in English, put in a paragraph of Spanish content without changing the "lang" attribute for that paragraph, and test it in a screen reader. You'll hear Spanish words read in an English/American accent, and many of the pronunciations won't be even close to correct. This is why the "lang" attribute is so important.