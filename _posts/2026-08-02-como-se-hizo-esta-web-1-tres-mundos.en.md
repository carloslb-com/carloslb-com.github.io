---
layout: post
lang: en
permalink: /blog/2026/08/02/como-se-hizo-esta-web-1-tres-mundos/
title: "How this site was built (1): one person, three trades, one website"
description: "Why a hybrid profile doesn't fit into a single-subject portfolio, and how three worlds can share one structure and only change their skin."
date: 2026-08-02 10:00:00 +0100
categories: [it]
tags: [Jekyll, Liquid, static site, Sass, bilingual site, web architecture, portfolio]
schema: BlogPosting
mermaid: true
---

I have three trades and one face. I work with systems and networks, I handle bookkeeping and paperwork, and I teach. A portfolio covering only one of the three would lie by omission; three separate portfolios would mean three maintenance jobs and none of them up to date. This series is about how I got out of that, what I decided and — above all — what I ruled out and why.

I started in early June 2026. The site went live on 22 July. In between there are a fair few decisions you can't see, and those are exactly the ones worth telling: **the value of a portfolio isn't in the list of technologies, it's in the reasoned trade-offs.**

All the code is out in the open: [github.com/carloslb-com/carloslb-com.github.io](https://github.com/carloslb-com/carloslb-com.github.io).

## The principle that ordered everything else

Before writing a single line I set myself a limit: **have something to show, rather than being 99.9% accurate.** A perfect portfolio that never ships isn't a portfolio, it's a folder. And a working motto: **robustness over brevity or cleverness.** Every time I hesitated between the clever solution and the boring one that holds up, the boring one won.

## The stack, and why

| Piece | Choice | Reason |
|---|---|---|
| Generator | Jekyll 4.4.1 (Ruby 3.3.8) | Static site: no database and no admin panel to attack |
| Styles | Dart Sass with `@use` / `@forward` | Real modules; `@import` is deprecated |
| Bilingual | jekyll-polyglot | Two trees (`/` and `/en/`) without duplicating templates |
| Extras | jekyll-feed, jekyll-seo-tag, jekyll-sitemap | The standard set, nothing invented |
| Environment | Ubuntu virtual machine on VirtualBox | Development isolated from my working computer |
| Publishing | GitHub Pages with a custom GitHub Actions workflow | Out of necessity, not preference: more on that in part three |

The important thing about that table is what **isn't** there: no database, no CMS, no third-party services embedded anywhere. A static site is a pile of HTML files. There's no session to steal and no query to inject.

## One person, three worlds

The structure is identical across the three profiles. Header, sections, blog, footer: the same. The only thing that changes is the **skin**: the palette and the typeface.

```mermaid
flowchart TD
  accTitle: Site structure, with a neutral landing page and three profiles
  accDescr {
    The landing page is a neutral space with three doors: IT and Telecommunications,
    Administration and Human Resources, and Training and Teaching. All three lead to the
    same page structure, and the only thing that differs between them are the CSS tokens
    that define the colour palette and the typeface.
  }
  H["Neutral landing page<br/>(three doors)"] --> IT["IT / Telecommunications"]
  H --> AD["Administration / HR"]
  H --> FO["Training / Teaching"]
  IT --> B["Same structure:<br/>header, sections, blog, footer"]
  AD --> B
  FO --> B
  B --> T["Only the CSS tokens change:<br/>palette and typeface"]
```

That's **eight palettes**: four worlds (the three profiles plus the neutral landing page) times two themes, light and dark. I validated them all at high contrast — most of them at AAA level — *before* writing a single line of content. Fixing contrast at the end means redoing everything.

The typefaces are self-hosted as `woff2`. The body text is **Atkinson Hyperlegible**, designed specifically for low vision. Headings change by world: JetBrains Mono for IT, IBM Plex Serif for Administration, Nunito for Training. A typeface says a great deal before the first word is read.

The data — projects, certifications, courses, work history — lives in YAML, following a `key → {es, en}` pattern. Only what actually changes between languages gets translated. A year is a year in both.

### A small decision with large consequences

The profile class lives on the `html` element, not on `body`, alongside the theme attribute. If it lives on `body`, the browser has already started painting by the time you apply the theme, and you get a flash of the wrong palette. With the class at the top, the script runs before there's anything to flash.

Side effect: because both attributes hang off the same element, the palette selectors are concatenated **without a space**. Yes, CSS has its own small print too.

## Colour can depend on JavaScript; navigation cannot

This is the decision I'm proudest of, and the one that ruled out the most.

The requirement was: if you enter the blog through the IT door, the article should *feel* like IT. But an article is a single file, and it can be reached from three places and in two languages.

**Path 1: generate physical versions of the article per context.** Three contexts times two languages is six versions of every article. Unworkable maintenance and duplicate URLs competing with each other. Ruled out.

**Path 2: have JavaScript rebuild the navigation bar on the fly.** More code, more fragile, and without JavaScript the visitor can't navigate at all. Ruled out.

**What I did:** the colour and the typefaces do change according to the door you came through; the navigation bar stays put.

```mermaid
sequenceDiagram
  accTitle: How an article takes on the colour of the door you came through
  accDescr {
    From the IT blog listing, the link to the article carries a parameter indicating where
    the visitor came from. The article is served with the neutral skin. A script placed in
    the document head reads that parameter before the browser paints anything, applies the
    matching profile class and removes the parameter from the address bar. The navigation
    bar never changes.
  }
  participant L as IT blog listing
  participant N as Browser
  participant A as Article
  L->>N: link carrying the origin parameter
  N->>A: requests the article (served with the neutral skin)
  A->>A: a script in the document head reads the parameter before painting
  A->>N: applies the IT skin and cleans up the address
  Note over N,A: The navigation bar never changes
```

If the script fails, the article shows up in neutral colours and reads perfectly. Nobody is locked out.

Two takeaways from that, which I've already reused elsewhere:

> **When every solution to a requirement is a bad one, sometimes the problem is the requirement, not the solution.**

> **Look for the version that delivers most of the perceived value for a fraction of the cost.** Colour gives you 90% of the sense of being in a different world. A dynamic navigation bar added 10% at enormous cost.

## How I worked on this

I didn't do it alone. I used an AI assistant as a tool: for reference, for learning Jekyll and Liquid, for diagnosis when something didn't add up, and for organising and tracking the tasks of a project that ran for two months and has a lot of moving parts.

I'm saying so plainly, because hiding it would be the exact opposite of what I stand for. And because the distinction matters: the tool speeds up research and keeps the work organised, but it doesn't make the decisions. The ones above — what to rule out, which requirement to question, where to stop — are mine, and each of them has its reasoning written down. In part three I'll tell you where it got things wrong and how I caught it.

---

**Next:** in part two, why this site doesn't load a single third-party resource, how the contact form works without JavaScript, and which regulations actually apply to a personal website — considerably fewer than the templates would have you believe.
