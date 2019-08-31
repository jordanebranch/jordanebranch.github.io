---
layout: post 
title: Introducing Snorkel, the Dive Design System
description: Our process for building a design system from scratch
date: 2019-06-13
categories: product
image: images/post/2019-06-13-introducing-snorkel/header.png
author: Jordan Branch, Natalie Forman
---

In the fall of 2018, Industry Dive began to transition from a scrappy startup model with hybrid front-end designers and backend developers to one with two scrum teams comprised of product designers and full-stack engineers.

With this transition came a number of issues.

<div class="grid-two-columns">
	<div class="grid-two-columns__list">
		<h4>Engineers</h4>
		<ul>
			<li>Were creating multiple versions of the same common components</li>
			<li>Continued to turn to our product designers for front-end guidance and ticket implementation</li>
			<li>Routinely had to navigate a complex set of SCSS partials and front-end code style guides</li>
		</ul>
	</div>
	<div class="grid-two-columns__list">
		<h4>Product designers</h4>
		<ul>
			<li>Spent a significant amount of time pair-coding or completing front-end development tasks</li>
			<li>Were not thinking globally and component-first when creating user interface (UI) mockups</li>
		</ul>
	</div>
</div>

To address these issues, the design team decided to build and maintain a design system for our publication websites.

When getting buy-in from Engineering, the team that would be using our design system, we laid out the following project goals and roadmap:

Design system goals:
- Enable developers to easily reference front-end code for common UI components
- Reduce bottlenecks and increase efficiency
- Provide a single source of truth

Design system roadmap:
1. Create a new SCSS style guide that engineers can easily reference, prior to the completion of the Design System
2. Create and roll out an MVP of the system with well-documented UI components and layouts
3. Create a more comprehensive Version 1.0 of our design system based on feedback from Engineering

After Engineering was onboard, we began to plan and build our MVP.

### Getting started

To kickstart the project, we made a list of UI components&mdash;e.g. alerts, buttons, etc.&mdash;that we commonly use throughout our publication websites. Although we planned to include design principles and guidelines, we focused on defining and creating reusable UI components first to maximize the practical value for Engineering.

After creating our MVP component list, we defined each component’s purpose&mdash;e.g. “Alert banners communicate key information, globally”&mdash;and determined if it was a stand-alone element (atom) or a group of smaller components (molecule). We also included two main design building blocks (utilities): color and typography.

Our initial list of components:
<ul class="list-two-columns">
 <li>Alerts (atom)</li>
 <li>Buttons (atom)</li>
 <li>Feeds (molecule)</li>
 <li>Form elements (atom)</li>
 <li>Labels (atom)</li>
 <li>Messages (atom)</li>
 <li>Sidebar boxes (molecule)</li>
 <li>Typography (utilities)</li>
 <li>Color (utilities)</li>
</ul>

### Auditing our components

Before creating a system with our list of MVP components, we needed to audit their current design and functionality on our live publication sites.
 
Our approach was comprehensive; we printed out every unique website page template that used an MVP component and taped the pages to a wall. We then sorted the pages into categories based on intended function&mdash;e.g. soft, medium, and loud calls-to-action. We quickly saw design discrepancies across our categories. Using these buckets, we defined design guidelines and rules for component variations.

<p class="centered">
    <img src="{{ site.url }}/images/post/2019-06-13-introducing-snorkel/wall-sorting.jpg" alt="Sorting the site"/>
    <span class="caption">The wall with button pages being sorted by action</span>
</p>

Example of our process for standardizing the “button” component:
1. Hang a printout of each website page template&mdash;e.g. topic page, contact page, etc.&mdash;that contains a button on the wall
2. Group the buttons based on the priority level of the action we want the user to take
 - Loud buttons: Primary action of the page or component and directly linked to core product KPI&mdash;e.g. Increase signups
 - Medium buttons: primary action of the page but not directly linked to core product KPI
 - Soft buttons: secondary action on a page
3. Define language and usage guidelines for all buttons
 - Use sentence case
 - Use as few words as possible in the CTA
 - Use for submitting content, not navigation
4. Define design guidelines for each variation
 - Loud buttons: use primary site color (can include an icon)
 - Medium buttons: use black and only on pages with forms as the main CTA
 - Soft buttons: use grey and never full-width

### Implementing the system
After the component audit, it was time to design and code the actual system. 

The build took place in three phases:
1. <strong>Technical implementation:</strong> Refactor the relevant code on our live publication sites
2. <strong>Sketch library:</strong> Create a Sketch UI component library for designers
3. <strong>Design system site:</strong> Implement an internal design system site for Engineering to reference

#### 1. Technical implementation
Following our live site audit, we began to refactor the relevant production code. This mostly involved updating SCSS class names and removing page-specific styling.

As part of the refactoring, we modified our SASS partials to be consistent with our new components. After lots of debate, we decided on a BEM approach. This entailed naming classes based on the component (block) and appending “--” for modifiers and “&#95;&#95;” for elements. After defining the style naming conventions, we applied them to the relevant components. We also deleted any page-specific styling that was being applied to the components. In the end, we eliminated a lot of code from our codebase, made styes more global in scope, and created a cohesive set of design patterns.

#### 2. Sketch library
After implementing the design system in the production codebase, we created resources for our product designers. We use Sketch for mockup creation, so we created Sketch libraries to share components across the design team. Sketch libraries allow designers to grab a component&mdash;e.g. button&mdash;with a predefined style and use it across multiple files. This ensures UI consistency and negates the need to recreate the same components with each mockup.

We set up the Sketch file system to mirror our production code structure. Each component has its own Sketch library file with core symbols for variations. We used Dropbox to host and version control the files.

<p class="full-width">
    <img src="{{ site.url }}/images/post/2019-06-13-introducing-snorkel/atoms.jpg" alt="Atomic elements in Sketch"/>
    <span class="caption">Atomic elements in Sketch</span>
</p>

#### 3. Design system site
After our design audit and Sketch library were complete, we created a dedicated website to make it easy for Engineering to reference the code and related documentation of all of our UI components. This site serves as a single source of truth for engineers, designers and all other internal employees.

The main requirements for our MVP launch were:
- An overview of Snorkel’s purpose
- Easy navigation to each component
- Component detail pages with guidelines and code snippets

We developed the site using our blog as inspiration for the technical architecture (Jekyll + Github pages). We then asked representatives from the Engineering team to review the site to ensure it met their needs.

With final approval from Engineering leadership, we formally rolled out the design system for our scrum teams to begin using.

Moving forward from this MVP, we plan to gather user feedback from our developers, write more detailed usage guidelines and explore ways to speed up our development process.

<span style="font-style: italic;">Originally published on [industrydive.design](https://industrydive.design/). Written in collaboration with [Natalie Forman](http://natalieforman.com/) and [Ryan McKnight](https://rtaylormcknight.com/).</span>
