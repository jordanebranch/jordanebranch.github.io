---
layout: post 
title: Redesigning the Industry Dive homepage
description: From concepts to front-end implementation
date: 2019-02-05
categories: product
image: images/post/2019-02-05-corpsite-home/header.png
author: Jordan Branch
---

Industry Dive recently updated its vision and mission statement to more accurately represent who we are today and who we aspire to be.

New mission statement: "Help decision-makers stay ahead in competitive industries by producing the business world's most respected journalism. Our insights spark innovation, fuel growth and shape agendas in every industry we cover."

As part of this branding project, our corporate website [homepage](https://industrydive.com) received a refresh.

After senior leadership made key decisions on copy for the new homepage, the design team had three weeks to draft mocks, secure stakeholder approval, implement the front-end code and deploy the updates. At the end of the three weeks, the founders planned to roll out the new vision and homepage at an all-hands company meeting.


### Design sprint


To accommodate the tight turnaround, we kick-started the design phase with a sprint session that involved the entire team – eight designers. The goal of the sprint was to quickly provide our two product designers with a wide range of layout and animation concepts from which to draw inspiration. An added benefit of the exercise was that it served as an opportunity for our graphic designers, who primarily work on content marketing projects, and our product designers, who primarily work on our web properties, to collaborate.


We modeled our design sprint off of a [GV sprint session](https://www.gv.com/sprint/) and structured it as follows:

1. **Generate ideas** – 10 mins – At the outset of the sprint, each member of the team wrote out ideas for a new corporate site homepage design – e.g. illustration-based sections, animated counters, video backgrounds, etc.
2. **Sketch** – 20 mins – Each designer folded a blank sheet of paper in half and, leveraging the ideas they listed, sketched a new homepage design concept in the two frames. Remote employees sent in a photo of their sketches. We then taped all of the sketches to a large window.
3. **Speed critique** – 60 mins – Each member of the team presented their sketches, and the entire group critiqued them.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-02-05-corpsite-home/sketches.jpg" alt="User flow iterations"/>
    <span class="caption">The team's sketches from the design sprint.</span>
</p>

### High-fidelity mocks

The sprint provided our product designers with concepts to draw from and build upon to craft a new homepage. To visually reinforce our identity as a modern business news publisher, we selected four overarching design patterns:

1. Significant whitespace so the user can focus on what is important
2. A typography-centered design to highlight our new messaging
3. Animation and accents of our brand color to emphasize important content
4. Imagery to provide additional visual context

Based on these patterns, we started drafting the first mock. We played with the size and placement of typography as well as the layout of the supporting copy. We also experimented with animation options and geometric accents.

After evaluating different layouts, we combined components from our individual designs into a final structure. This structure was then passed off to a senior graphic designer to “bring our personality,” one of the company’s core values, to the page.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-02-05-corpsite-home/graphics.png" alt="User flow iterations"/>
    <span class="caption">Different iterations of high fidelity mocks.</span>
</p>

### Designing the motif

With the layout finalized, the team set out to find a visual motif that would both differentiate our brand from the competition and also unify the page. The motif needed to be:

1. In line with our new messaging
2. Easily replicated for use throughout the site, not just the homepage
3. Inclusive enough to support our multiple industries

After some serious deliberation, we landed on a chevron as the primary visual symbol. To us, the chevron represents progression and Industry Dive’s goal of moving industries forward.

Our first step was to place chevrons at the beginning of important paragraphs to help direct user attention. We then put our brains together to figure out how we might be able to subtly incorporate the chevron in the white space throughout the homepage. At first, we considered placing a large chevron in the background, but that idea was dropped in favor of using simple lines angled like the sides of a chevron. We believed this motif would visually unite the site and guide the user through the content.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-02-05-corpsite-home/motif.png" alt="User flow iterations"/>
    <span class="caption">A few of the options for the design motif.</span>
</p>

After finalizing the motif, we discussed whether to incorporate imagery or mostly rely on the chevron concept. We decided to include a pair of small accent photos to help anchor the content and lead the reader through the sections. Although we initially planned to use black and white images, we ended up with two full color photos, similarly edited, to make the page feel more inviting.

We believe the pictures we selected exemplify the diversity of our executive readership while remaining industry-agnostic.


### Adding emphasis to key messaging with animation

After we infused the page with a strong visual motif to strengthen our brand, we looked for ways to draw site visitors’ attention to the most important points of the new messaging:

1. Industry Dive’s business journalism shapes agendas and sparks ideas for industry leaders
2. Our readers are powerful industry voices who marketers want to reach
3. We are in 16 industries and counting

While we wanted to use animation to emphasize these main points, we did not want any movement to distract from the content. For a smooth transition, the team elected to use variations of fade-in events.

All three sections required a slightly unique experience to fit the information being presented.

The above-the-fold section introduces our mission statement, the core of our new messaging, which can be broken down into three taglines. Each tagline can stand alone but are more powerful when juxtaposed. We opted to fade them in and out individually, putting emphasis on one at a time.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-02-05-corpsite-home/topsection.gif" alt="User flow iterations"/>
    <span class="caption">The animation for the top section of the page.</span>
</p>

The next section, directed toward marketers, describes the audience our business journalism reaches. We opted for an ordered list of statements about our readers that would entice potential clients to work with us. For emphasis, each list item fades in, one by one, with a slight delay.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-02-05-corpsite-home/middlesection.gif" alt="User flow iterations"/>
    <span class="caption">The animation for the middle section of the page.</span>
</p>

In the third and final section, we wanted to call out the number of industries we cover. To highlight our growth, the number fades in and counts up.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-02-05-corpsite-home/bottomsection.gif" alt="User flow iterations"/>
    <span class="caption">The animation for the bottom section of the page.</span>
</p>

To tie all of our animations together in a cohesive experience, we applied a fade in on scroll effect to our images.

### Next steps

With our updated homepage design live, we now plan to create a design system for the entire site that incorporates our new styles. A design system will ensure we maintain a high-quality user experience and strong brand consistency across all pages.

<span style="font-style: italic;">Originally published on [industrydive.design](https://industrydive.design/). Written in collaboration with [Natalie Forman](http://natalieforman.com/) and [Ryan McKnight](https://rtaylormcknight.com/).</span>
