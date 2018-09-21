---
layout: page
parent: "Components"
title: "Breadcrumbs"
intro: "Breadcrumbs are a navigation element used to help orient a user within an application, and enable quick access to a parent level."
jump_menu: true
---

<div class="ds-preview">
  <div class="treas-breadcrumb">
    <nav class="treas-breadcrumb__nav" aria-label="Breadcrumbs">
      <ol class="treas-breadcrumb__list">
        <li class="treas-breadcrumb__item">
          <a href="#" class="treas-breadcrumb__link">Home</a>
        </li>
        <li class="treas-breadcrumb__item">
          <a href="#" class="treas-breadcrumb__link">Level 1</a>
        </li>
        <li class="treas-breadcrumb__item">
          <a href="#" class="treas-breadcrumb__link">Level 2</a>
        </li>
        <li class="treas-breadcrumb__item">
          <a href="#" class="treas-breadcrumb__link">Level 3</a>
        </li>
      </ol>
    </nav>
  </div>
</div>
```html
<div class="treas-breadcrumb">
  <nav class="treas-breadcrumb__nav" aria-label="Breadcrumbs">
    <ol class="treas-breadcrumb__list">
      <li class="treas-breadcrumb__item">
        <a href="/" class="treas-breadcrumb__link">Home</a>
      </li>
      <li class="treas-breadcrumb__item">
        <a href="/level-1/" class="treas-breadcrumb__link">Level 1</a>
      </li>
      <li class="treas-breadcrumb__item">
        <a href="/level-1/level-2/" class="treas-breadcrumb__link">Level 2</a>
      </li>
      <li class="treas-breadcrumb__item">
        <a href="/level-1/level-2/level-3" class="treas-breadcrumb__link">Level 3</a>
      </li>
    </ol>
  </nav>
</div>
```

## Usage

### Use When

* Displaying hierarchy.
* The application structure is several levels deep.
* You want to allow the User to navigate quickly to various levels within the application architecture without using the browser back button.
* You want to help orient the User and provide contextual awareness within a process or application structure.

### Don't Use

* To display History.
* To reflect a multi-step process.
* Within the page content as a hyperlink feature.
* If the application is only one level deep or if the global navigation's first level can be used.

## General Guidance

* Breadcrumbs are marked up an an Ordered List (`<ol>`) as its order matters.
* Breadcrumbs should be located just below the global navigation system and above the main content of the application.
* Keep each crumb's title brief but descriptive.

## Accessibility

* Note the use of the `<nav>` element and `aria` attributes to describe the type of navigation.