# Shopify Starter Theme with Webpack
12/14/2021 - Initial Setup  
This is a minimal bare bones Shopify starter theme.

## Features
1. Basic Webpack setup
    1. Webpack will transpile Sass to CSS and bundle Javascript files
2. Custom CSS Framework
    1. The CSS framework comes with a 16-column grid and a bunch of utility classes
3. Compatible with both Theme Kit and Shopify CLI

## Notes
This will never be a complete Shopify theme. That's not the goal. The goal is to provide a boilerplate for quickly getting you to the point where you can start developing with minimal config. I plan on adding to it but I don't have much free time right now, so I don't know when that will be. Do you remember the old Slate theme? Well, this one has even less stuff- it's a blank slate! * *drum shots* *

It's preferable that this is used by developers already familiar with Webpack and Shopify because I don't have time to write up proper documentation.

There is probably lots of room for improvement. As of today it's all working as expected though. If you want to help me with this project I totally welcome that. I can't promise that I will accept all PRs, though, because I am going to be a little picky about this project. And if you fork this please give me credit.

## Useage
A brief how-to:
1. start Theme Kit or Shopify CLI from the root *shopify-starter-theme-with-webpack* dir
2. start Webpack from the root *shopify-starter-theme-with-webpack* dir
3. customize theme files like you normally would
4. Sass and Javascript are stored in **src/styles** and **src/scripts**
    1. when changes are made in there, webpack will transpile and bundle and then whichever Shopify tool you're using, to watch the theme files, will upload to Shopify.
    2. **Required:** use [Sass modules](https://sass-lang.com/blog/the-module-system-is-launched) (e.g. **@use** and **@forward**) when working with the Sass files
        1. Follow the patterns that area already in place
        2. Examples:
            1. if you need access to the variables then pull them in with **@use**
            2. if you create a new .scss file then the index will need to be updated with a new **@forward** statement
5. when you're done customizing, stop webpack from watching and then run a build. If you keep Theme Kit or the CLI running when you build, then the minified files will get uploaded to your theme.
6. do your usual git and deployment steps
7. repeat

The CSS Framework:
1. The CSS Framework that comes with this starter theme is my own project. I built it. Not from scratch, but I did put *a lot* of work into it. It started out as Bootstrap 5 and then I heavily modified it. I ripped out all the stuff that I rarely use and then I started customizing it to make it my own. It has been used in several site builds and I think it works out quite well. I don't have a repo set up for it yet but I'll do that when I get time and then I'll update this with the link.
2. The grid uses the standard architecture: **.container > .row. > .col-4**
3. The utility classes can be found in **/src/styles/global/utilities.scss**
4. These are the Breakpoints:
    1. min-width: 640px - **Small** (sm)
    2. min-width: 896px - **Medium** (md)
    3. min-width: 1152px - **Big** (bg)
    4. min-width: 1408px - **Large** (lg)
    5. min-width: 1664px - **Extra Large** (xl)
    6. min-width: 1920px - **Extra Extra Large** (xxl)
