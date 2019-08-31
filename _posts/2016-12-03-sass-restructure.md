---
layout: post 
title: Restructuring our Sass
description: Breaking down our Sass architecture into more maintainable parts
date: 2016-12-03
categories: product
image: images/post/2016-12-03-sass-restructure/sass-header.jpg
author: Jordan Branch
---


When Industry Dive first built its publication sites, the Sass was written in a single stylesheet, organized with section headings and a table of contents. After the site was live, the team re-evaluated its Sass architecture and decided to break it up into more maintainable parts. This decision allowed us to see any code bloat and more efficiently update styling.

There are many resources out there for Sass architecture. [Smacss](https://smacss.com/) is a popular philosophy for breaking down Sass. Sitepoint had a useful [blog](https://www.sitepoint.com/architecture-sass-project/), as well. David Khourshid also offers some [insight](https://scotch.io/tutorials/aesthetic-sass-1-architecture-and-style-organization) and, of course, there’s always [The Sass Way](http://thesassway.com/beginner/how-to-structure-a-sass-project), a resource for everything Sass related.

The common theme that appeared in all of their recommendations: Break your sass down into reusable parts. The goal is to eliminate page-specific styling and reduce code bloat.

Drawing from the best practices of several leading tech companies, I worked with the team to create a directory structure that fit the needs of our business and the way we code at Industry Dive.

Here is an overview of what the team came up with:
- Base (Sass i.e. variables and extendables)
- Components (reusable parts of the site i.e. forms, buttons, accordions)
- Layout (sections of the site that make a wireframe of its overall structure i.e. sidebar, footer, menu)
- Pages (custom full-page templates that appear on the site)
- Utils (universal tools and settings for the site i.e. helper classes and typography)
- Vendor (third party sass sheets i.e. Foundation’s grid and normalizer)

Within each folder is a sass partial named after the folder that imports the rest of the partials that fit that folder’s category. These top-level files are then imported into the final Sass sheet, which will be compiled to our css. While front-end developer Jessica Bell’s Sass architecture is slightly different than the one we finally chose, she offers a great [starting point repository](https://github.com/sirjessthebrave/minimal-site) on Github.

Now that we can see our code more clearly, the team is conducting an audit of it. About halfway through the clean up, we have deleted a ton of unnecessary code and streamlined the way we are styling elements across the site — denesting and using fewer classes while styling HTML elements directly.
