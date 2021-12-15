# Shopify Starter Theme with Webpack
12/14/2021 - Initial Setup  
This is a bare bones minimal Shopify starter theme. It comes with a basic Webpack setup and a custom CSS Framework.
Webpack will transpile Sass to CSS and bundle Javascript files. The CSS framework comes with a 16-column grid and a bunch of utility classes. This is also compatible with both Theme Kit and Shopify CLI.

This will never be a complete Shopify theme. That's not the goal. The goal is to provide a boilerplate for quickly getting you to the point where you can start developing with minimal config. I plan on adding to it but I don't have much free time right now, so I don't know when that will be. Do you remember the old Slate theme? Well, this one has even less stuff- it's a blank slate! * *drum shots* *

It's preferable that this is used by developers already familiar with Webpack and Shopify because I don't have time to write up proper documentation.

There is probably lots of room for improvement. As of today it's all working as expected though. If you want to help me with this project I totally welcome that. I can't promise that I will accept all PRs because I am going to be a little picky about this project. And if you fork this please give me credit.

A brief how-to:  
1. start Theme Kit or Shopify CLI from the root *shopify-starter-theme-with-webpack* dir
2. start Webpack from the root *shopify-starter-theme-with-webpack* dir
3. customize theme files like you normally would
4. Sass and Javascript are stored in *src/styles* and *src/scripts*
    1. when changes are made in there, webpack will transpile and bundle and then whichever Shopify tool you're using, to watch the theme files, will upload to Shopify.
    2. **Required:** use [Sass modules](https://sass-lang.com/blog/the-module-system-is-launched) (e.g. *@use* and *@forward*) when working with the Sass files
        1. Follow the patterns that area already in place
        2. Examples:
            1. if you need access to the variables then pull them in with *@use*
            2. if you create a new .scss file then the index will need to be updated with a new *@forward* statement