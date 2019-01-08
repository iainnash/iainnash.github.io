---
title: GoCardless
when: 2015
type: internship
summary: built an localized and international isomorphic React marketing site, built a AJAX testing stub library and built a PHP API template
link: https://gocardless.com/blog/interning-at-gocardless/
more: true
---

From [Interning at Gocardless Blog Post](https://gocardless.com/blog/interning-at-gocardless/)

# Interning at GoCardless
I'm wrapping up a four month internship at GoCardless and thought I'd share some of the projects I've worked on.

GoCardless has a real variety of projects, which has kept every day interesting and challenging. From front-end javascript to PHP client libraries, I've worked on almost everything at GoCardless and been able to learn from some awesome developers. Here are a few highlights:

## React / How I came to love React
A couple of months ago we decided to rewrite the GoCardless marketing pages using React to support proper internationalisation. I was on the team from the inception of the project, figuring out how the app would work and seeing it through to completion.

Since last summer I'd been hearing great things about React, so it was great to get an opportunity to give it a try. We rewrote the site into an isomorphic site based off of dynamic React components, and I was really impressed by the flexibility and speed of the framework - both in development and production. GoCardless is planning to open source the work, and I'll definitely use React again.

## Query Counting / How hard can a count be?
While working on the GoCardless dashboard I saw a few cases where having a count in the API responses would improve search and exports. Knowing if your search has two or two hundred pages can be helpful! I chatted to the team, and set about adding it.

As it turns out, getting a precise count isn't so straightforward. The API is built for queries that could match millions of rows, and needs to quickly return the paginated collection. After a few experiments with count optimisation and estimate counting in PostgreSQL I worked with the Platform team and we settled on using an exact count up to a limit. It was great to dig a bit deeper into the limits of PostgreSQL, and to figure out a pragmatic solution.

## Stubby / Hijacking XMLHttpRequests for fun and profit
Internally, GoCardless uses JSON Schema extensively - all API requests are validated against a schema, and the GoCardless Pro docs are auto-generated from it. In my last couple of weeks at GoCardless I worked on adding another use for JSON Schema - stubbing out API requests in front-end app's tests, additionally validating that the requests themselves are valid.

There's more detail about Stubby, which is our open-source solution to the above, here. It was great to build something open-source, and I learned a lot about the process (docs, tests, READMEs and config all suddenly became much more important). I'm really glad that GoCardless as a company is invested in open source and emphasises giving back to the tech community as a whole, looking beyond their own product.

## PHP Library / When I thought I was done writing PHP
Finally, when I started this internship I wasn't expecting to write any PHP. Even stranger, I wasn't expecting to write any PHP in Go...

A lot of our customers were requesting a PHP library for the new GoCardless API, so I stepped up to build one. GoCardless auto-generates all its Pro client libraries using an internal tool (soon to be open-sourced) called Crank, which combines Go template files with a JSON Schema to build a library.

I'll be honest, working with PHP was a bit of a hassle! In many cases we were torn between writing idiomatic PHP and making the library consistent with GoCardless libraries in other languages (we generally chose the former, but the trade-off in maintainability is very real). Some of PHP 5.3's new object oriented features such as magic methods and namespaces allowed for decent workarounds, but it was certainly tricky to make the decision of using them. Having put a lot of thought and effort into it the most satisfying part of the project was seeing integrators using the library immediately, and being able to respond to their feedback.

