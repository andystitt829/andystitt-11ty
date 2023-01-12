---
title: 'Lessons learned in my accessibility journey'
description: 'You can make a huge difference in your web development career if you focus on web accessibility.'
date: 2023-01-12
---

As of this writing, I have been focusing on accessibility as part of my job as a web developer for almost two years.

The only thing I knew before then was that I was supposed to write alt text for images, and even then I did it very badly ("Picture of [insert image subject here]" is not very descriptive).

Over the last two years, I have learned about [WCAG success crtieria](https://www.w3.org/TR/WCAG21/), automated and manual testing, prioritizing accessibility as early in the process as possible (as in right away), and just having people with disabilities at the top of my mind as I build things that people will use.

Here are the major lessons that I've learned in my accessibility journey:

## Accessibility is everybody's job

WCAG stands for Web Content Accessibility Guidelines. Everyone that has anything to do with building a website and putting content on it is responsible for the content's accessibility.

Lots of people think that accessibility is the developer's job only. WCAG does not stand for Web Code Accessibility Guidelines. Code is part of the content, but developers are not the only ones responsible for accessibility.

So are designers. So are content writers and editors. So are their managers. So are the company leaders.

Every single person who has anything to do with building a product that people use is responsible for accessibility.

## There is so much work to do

Even though the WCAG standards have been around for over 20 years, way too many people don't pay attention to them and develop websites for sighted, able-bodied, neurotypical users who use a web browser, a keyboard, and a mouse to navigate websites. How people with disabilities would interact with their websites never even crosses their mind.

That's why there is so much work to do.

It took the pandemic to even bring accessibility to my attention, and since then, [hiring for accessibility specialist roles has increased](https://www.wsj.com/articles/more-companies-are-looking-to-hire-accessibility-specialists-11630501200).

It's a shame that this didn't happen sooner. It's wild to think that I was only ten years old when the Americans with Disabilities Act was passed in 1990. Historically, and I can only speak for my home country of the United States, disabled people have not been treated well. Their lives have not been valued.

Even with the ADA being over 30 years old and the WCAG standards being over 20 years old, there is still so much work to do and so many inaccessible websites to fix and new accessible websites to be built.

The work has to be done, and we must do it, together, collectively. There is no other option.

## There is so much low-hanging fruit

As developers, one of the strongest tools in your box for writing accessible code is semantic HTML. Things like `<header>`, `<main>`, and `<footer>`, which help assistive technologies announce to the user what section of the website they're in, are incredibly helpful and simple to implement.

Because of the proliferation of the use of JavaScript and its frameworks, and social media influencers and gatekeepers saying that HTML isn't "real programming", there are so many applications that have inaccessible HTML.

Another example that I've had to deal with is the lack of use of the `<button>` tag. I have seen what is supposed to be a button coded using `<span>` tags and the button's functionality programmed using JavaScript.

The problem is that the JavaScript that was used only accounted for mouse clicks. Not everyone uses a mouse. Some people only use their keyboard. When I tabbed to the button using my keyboard and then tried hitting the return key and spacebar, nothing happened.

Instead of programming functionality for a `<span>` tag, you can use a `<button>` tag which browsers and assistive technologies already recognize and know what to do with it. No extra functionality needed.

There's a lot of low-hanging fruit like this just with fixing semantic HTML. You can make small and large improvements just by fixing these kinds of things up.

## You need disabled user testers to validate the accessibility of your websites

I am now at the stage where I need to work with disabled user testers on the websites that my team builds.

My team is so conscientious of accessibility now that, while we're not perfect and we miss things, we hit a whole lot of our marks. I find myself having conversations with one of my fellow developers about the best way to build a particular interface to make it as accessible and usable as possible.

We test what we build with screenreaders and ponder if there's anything that we're missing.

The fact is: we don't know because we're not native screenreader users and we're not disabled website users. We have gone as far as we can with making sure that we have the bare minimum of accessibility covered, and now we need disabled user testers to help take our websites' accessibility and usability to the next level.

One thing that I have heard the disability community repeat when it comes to people who build websites and focus on accessibility: "nothing about us without us." Of course. That makes perfect sense. If we're focusing on building websites that people with disabilities can access, then of course people with disabilities should be in the room.

## Come jump on the accessibility train!

Those are the biggest lessons that I've learned since diving into accessibility almost two years ago. When you first jump in, it can seem really intimidating. There's so much to do and so much to know.

But you're not alone. You can't do it alone. It's not your responsibility to do it alone.

Do your best to find people who are also dedicated to making the web a more accessible place. It could be at your job. It could be in online communities. Feel free to reach out to me at one of my social media links in the footer of this website and let me know if you have any questions!