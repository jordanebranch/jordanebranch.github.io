---
layout: post 
title: When and how I use classes in SASS to maintain a clean front-end codebase
description: After our new publication sites were live, the team re-evaluated its Sass architecture and decided to break it up into more maintainable parts.
date: 2018-04-01
categories: product
image: images/post/2018-04-01-sass-classes/class-header-image.jpg
author: Jordan Branch
---

When I started at Industry Dive, I lead the team in re-examining how we organized our SASS. As discussed in a previous blog, we went from one SASS stylesheet to organizing our styles into partials. This created a component-driven system that then paved the way for cleaning unnecessary code and putting measures into place to ensure we wouldn’t have a mess again. 

The overarching strategy is to make our code as global in scope as possible and where it cannot be, as reusable and contained as possible.

One of the main ways we achieve this is by judiciously using and naming our classes. At the top level, each component on our site is defined by a semantic class name. This class name should tell the developer exactly what the component is (i.e. breadcrumb, sidebar-box, button, progress-bar).

Within that component, our front-end designers use HTML to structure the component’s content. Our SASS builds off of this clean, minimalistic HTML. Where we can target a semantically named HTML element in our SASS without a class, we do. For example, an img tag in an element containing a single image, indicates the one image in that component. A div or a span that could be holding any number of elements would need a class. 

{% highlight css %}
.card {
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
    margin-bottom: 1.5rem;
    transition: all 0.2s ease-in-out;
    img {
        width: 100%;
    }
    p {
        margin: 0; 
        padding: 1.25rem 0; 
        text-align: center;
    }
    &:hover {
        box-shadow: 0 8px 18px rgba(0,0,0,0.10), 0 6px 6px rgba(0,0,0,0.18);
        cursor: pointer;
        transition: all 0.2s ease-in-out;
    }
}
{% endhighlight %}

When we want our SASS to be specific to one component, we can rely on SASS to compile down into element-specific css. That is to say when writing class names for elements inside of components, we don’t reiterate the component name. 

<span style="color: green; font-weight: 900; margin: 1.5rem 0 -0.75rem 0; display: block;">GOOD</span>
{% highlight css %}
.label {
    color: $dive-grey-5;
    font-size: .875rem;
    overflow-wrap: break-word;
    text-transform: uppercase;
    word-wrap: break-word;
    &.sponsored {
        color: $sponsored-color;
        font-weight: 600;
    }
    &.editorial {
        color: $primary-color;
        font-weight: 700;
    }
    &.opinion {
        color: #000;
        font-weight: 700;
    }
}
{% endhighlight %}

<span style="color: #d62828; font-weight: 900; margin: 1.5rem 0 -0.75rem 0; display: block;">BAD</span>
{% highlight css %}
.label {
    color: $dive-grey-5;
    font-size: .875rem;
    overflow-wrap: break-word;
    text-transform: uppercase;
    word-wrap: break-word;
    &.label-sponsored {
        color: $sponsored-color;
        font-weight: 600;
    }
    &.label-editorial {
        color: $primary-color;
        font-weight: 700;
    }
    &.label-opinion {
        color: #000;
        font-weight: 700;
    }
}
{% endhighlight %}

This is the bread and butter of how we keep front-end designers from opening up partials at christmas time and finding socks instead of that brand new bike. However, there is always room for improvement. 

The next step would be to get our back-end developers on board with understanding our class names by creating a product language. For example, is an editorial story an article or a post? To be continued...

