---
title: "Tailwind CSS: A Pragmatic Choice for Faster UI Development"
description: "Understanding the Benefits, Trade-offs, and Adoption of Tailwind CSS"
publishDate: "4 March 2024"
tags: ["css", "tailwind", "web development"]
coverImage:
  src: "./tailwind.webp"
  alt: "Tailwind CSS logo"
---

## <a id="intro-beyond-framework-wars" href="#introduction-beyond-the-framework-wars" class="markdown-heading">Introduction: Beyond the Framework Wars</a>

Another day, another Tailwind post and a new JS framework coming out (very likely). As a disclaimer, this isn’t a "Tailwind vs X" article or an attempt to convince anyone to switch over to where the grass is greener. Instead, my aim is to share and explore what I've seen Tailwind get right, what teams benefit most from it, and why it gained traction in the first place.

As developers, we often feel obliged to defend our trusty tools, frameworks, and libraries. While I do sometimes have stronger opinions on which tools are better suited for particular problems and situations, UI styling is just one of those areas of web development where there are so many options available that you could spend a lifetime simply trying out all the potential libraries and frameworks that allow to make your UIs pretty and pleasant to use. I won't attempt to persuade you to ditch your current styling solution for Tailwind and pretend it will fix all your problems related to styling UIs. Like all other tools and technologies in software engineering, analyzing and choosing well primarily depends on context and requirements. So Tailwind may not fit your team needs if the project has been using SCSS for the past 5 years and switching over means migrating 500 scss files. Ok then, preamble over so let's talk some Tailwind.

Tailwind serves a purpose and fills a void that has been present in the UI world for some time now. Before Tailwind, teams had to:

- Write and maintain large, and _many times_ bloated CSS files.
- Deal with specificity issues and cascading conflicts.
- Come up with and enforce naming conventions (e.g., BEM, SMACSS) to keep CSS manageable and readable.

All of the above challenges are not necessarily problematic if you have a standardized approach and system that “forces” developers to follow the rules of your custom CSS “pseudo-framework.” The issue is, very few FE teams can check that box. Many teams roll their own styling systems, but few have the deep design expertise to cover all that makes up a robust and complete styling solution/framework. This leads to inconsistent and unintuitive CSS solutions that are half-baked and become another maintenance burden for developers.

So, how can Tailwind help in this situation? First, let's briefly attempt to define it. In short, it is a utility-first CSS framework that offers many builtin options to style UIs. It has an arguably solid developer experience, a mature ecosystem, wide adoption, and integration with most of the popular web frameworks (Next.js, Phoenix, Laravel, Astro, RoR). I’ve been using it professionally for the past 3 years, and for the most part, it has been a nice and enjoyable experience. It has helped me build and ship UIs faster, more consistently, and has reduced the need to dive too deep into CSS quirks.

## <a id="tailwind-landscape" href="#the-tailwind-landscape-lovers-skeptics-and-critics" class="markdown-heading">The Tailwind Landscape: Lovers, Skeptics, and Critics</a>

Are companies, teams, and developers even using Tailwind? How has the industry responded to it? It seems the sentiment towards Tailwind is mixed. Some developers are using Tailwind and genuinely love it, others may be considering giving it a test drive to see what all the fuss is about, and there are yet those who will die on the "Tailwind turns HTML into an unreadable mess" hill. Honestly, Tailwind is not for everyone. And the utility classes can make your HTML look a bit noisy and cluttered. Spoiler alert, there are ways to clean up long and bloated classes if that is your pet peeve. There's this pattern:

Define:

```css
/* styles.css */
.btn {
	@apply rounded bg-blue-500 px-4 py-2 text-white hover:bg-blue-600;
}
```

Use:

```jsx
<button className="btn">Click me</button>
```

We all have our philosophies, beliefs, and preferences when it comes to tech tools and approaches. I get it. Some people prefer to write raw CSS or use a preprocessor like SCSS. That’s fine. Tailwind is not a silver bullet, and it has its own set of trade-offs. It has its own set of limitations. But it is a pragmatic choice for many teams and developers who want to ship UIs faster and more consistently with a system that just works. These benefits are hard to ignore, especially for small teams and startups that need to move fast and iterate quickly. Tailwind is a great choice for them. Loads of tech companies, early startups, and solo devs are building and shipping their UIs using Tailwind. And they are having success doing it.

## <a id="tailwind-stand-out" href="#what-makes-tailwind-stand-out" class="markdown-heading">What Makes Tailwind Stand Out</a>

Probably Tailwind’s biggest selling points are customizability, good built-in defaults, un-opinionated styles, speed of development, and documentation. It provides a standardized system of utility classes and design tokens, covering colors, typography, layouts, spacing, responsiveness, positioning, sizing, dark mode, and much more. You can customize the theme configuration or stick with the default—up to you. This is great.

Before Tailwind came onto the scene, creating a custom design system meant either hand-rolling it with raw CSS or a preprocessor, or adopting a full-fledged UI component library like Material UI, Bootstrap, Chakra UI, etc. With most UI libraries, adopting one meant locking yourself into their predefined styles.

Tailwind, however, took a different approach. It said:

> Naming CSS classes, managing rules, and handling specificity conflicts is a hassle. Here are utility classes you can inline to cover most common use cases, so you don’t have to worry about styling overhead or remembering class names. We’ll also tree-shake unused styles in production to improve performance. Plus, you can easily build your own theme and design system using our primitives, or just use our default theme. Up to you!

It became the missing answer for teams and companies who lacked deep CSS expertise but also did not want to pay the cost of getting married to a pre-styled UI component library (although TW does play nicely with things like Material UI) just to reap the benefits of a production-ready CSS theme and design system. Tailwind came in and filled that gap, which helped tons of developer teams build UIs faster. Its impact on the developer community and the industry as a whole is undeniable.

## <a id="tailwind-tradeoffs" href="#the-trade-offs-tailwind-vs-alternative-approaches" class="markdown-heading">The Trade-offs: Tailwind vs. Alternative Approaches</a>

Can you achieve the same with raw CSS, SCSS, or even another CSS framework? Absolutely. Have a ton of successful tech companies built UI products with just raw CSS and no other styling abstractions? Surely. But understand the tradeoff you are making. It takes significant time and effort to properly build a styling & design system. You then also have to onboard new developers to your custom system. This is time and effort that could be spent on building features and shipping products.

I was unfortunate enough to work on a handful of projects that had their design system built on raw CSS, and I still get war flashbacks from the over-engineered and just outright clunky ergonomics they offered. Developer experience was an afterthought. Frankly, I don’t blame the authors of those custom design systems and styling abstractions; frontend development is complex, and we’re juggling a lot of different responsibilities. Tailwind understands this and helps lighten the load.

Its true value lies in its convention—a widely adopted, standardized approach that many teams and organizations have converged on. The developer experience, with inline comments on utility classes that clearly indicate which CSS is being applied, is seamless and intuitive. The Tailwind team understands developer pain points and works to minimize them.

## <a id="bigger-picture" href="#the-bigger-picture-developer-experience-and-team-productivity" class="markdown-heading">The Bigger Picture: Developer Experience and Team Productivity</a>

Other utility-first CSS frameworks exist, such as UnoCSS, AtomicCSS, and many more. I chose Tailwind for this article because it is widely known and needs no introduction. The way I like to frame it and think about it is, Tailwind’s value is in the system it provides. It offloads decisions on how to style UIs, which ultimately helps many small and resource-constrained teams get up and running quickly and ship faster. Once you’re familiar with it, working in other Tailwind based projects becomes seamless, eliminating the need to learn custom styling abstractions and wasting onboarding time.

That said, if you’re a CSS expert and have already built a scalable, standardized approach within your team, more power to you. Like everything in software development, what you choose to use depends on your own context, needs, and experience.

Happy hacking!
