## Overview

For this assignment, we created the same webpage layout in two different ways. One version uses Flexbox (`index-flexbox.html` and `flexbox-style.css`), and the other uses Grid (`index-grid.html` and `grid-style.css`). Both versions use `base.css` for the colours, fonts, and common components. The main difference is how the page layout is created.

## Which was easier to implement?

Grid was easier for the main page layout. After naming the areas (`"left main right"`), we could easily change the layout at different screen sizes by changing the `grid-template-areas` and columns.

Flexbox was easier for smaller parts of the page that mainly go in one direction. For example, the header, navigation bar, and footer were simple to create using `display: flex` and `gap`.

## Which required less code?

Grid required less code when we needed a layout with both rows and columns. For example, the card gallery could be created with one simple rule:

`repeat(auto-fit, minmax(min(14rem, 100%), 1fr))`

This meant we did not need extra media queries for the cards.

The Flexbox version needed more CSS rules to control the sizes and positions of the items. We also needed extra rules for wrapping, changing the order of items, and changing the layout on smaller screens.

Some Flexbox rules were also needed to cancel or change earlier rules when the screen became smaller. This made the CSS longer and a little harder to manage.

## Which was more intuitive?

At first, Flexbox was easier to understand. It is simple to think about putting items in a row or column and allowing them to take up available space.

Grid seemed a little harder at first because it focuses on the whole page structure. However, once we used names such as `"left main right"` in `grid-template-areas`, the CSS became easier to understand because it looked similar to the page design.

Grid also allowed us to keep the HTML in a good order for screen readers and keyboard users while changing how the items looked on the page. With Flexbox, using `order` only changes the visual order, which can sometimes be confusing.

## When would we prefer one over the other?

We would use **Flexbox** for:

- Navigation bars
- Toolbars
- Groups of buttons
- Centering items
- Small components that mainly need to be arranged in one direction

We would use **Grid** for:

- The main page layout
- Layouts that need rows and columns
- Pages that change structure at different screen sizes
- Card galleries
- More complex two-dimensional layouts

## Analysis

Flexbox and Grid are both useful, but they are good for different things.

Flexbox is mainly about arranging content in one direction, either in a row or a column. The items can adjust their size depending on the available space.

Grid is more focused on creating the structure of the page first. We can define rows and columns and then place content inside them.

For this project, Grid was easier and required less code for the main page layout. Flexbox was still very useful for smaller parts of the page.

The best solution was to use both: **Grid for the main page structure and Flexbox for smaller components.**
