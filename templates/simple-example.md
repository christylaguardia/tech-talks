<!-- Use this template when your project is not very complex and difficult. -->

# Project Name TDD

Author: ?

## What are you building?

<!-- Describe what problem are you trying to solve, what you are trying to build or what it is you are trying to do. Give an overview of the functionality. -->

I really like to cook, but I'm also very disorganized. I'd like to have a better way to read my recipes.

I will create a simple website for viewing my recipes.

## How are you going to build it?

<!-- Show how you are going to build it. You can list the steps or explain the final state. If it applies, include any diagrams, wireframes, pseudo-code, or code snippets that validate your design. Make sure to include details for any areas that are especially complex or risky. -->

I'd like to use the Jamstack for this, which includes:

1. Pre-rendering static html with a popular framework like Gatsby, Hugo or NextJS. See [this guide](https://jamstack.org/generators/).
2. For the MVP, I won't and any special JS or any external APIs.
3. The data itself could be hardcoded JSON files for now.
4. Eventually, I might want save the content in a database or use a Content Management Systems (CMS) like Contentful.
5. I'd like to de-scope complex deployments right now, and just something simple like GitHub pages.

## Why are you building it that way?

<!-- Explain the reasons why are you solving the problem this way. Include any considerations to alternative approaches or options. -->

Given the high volume of cooking I do, I need a site that will load fast. Static pages are very fast.

I could skip the framework and just write the recipes in regular HTML files, but I'd like to avoid future time consuming work from moving the recipes from html to a database or CMS.
