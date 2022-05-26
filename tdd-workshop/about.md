# Technical Design Document Workshop

This is a workshop designed to teach beginners how to write a Technical Design Document (TDD).

<details>
  <summary>About</summary>
  I'm a Senior Software Engineer at ClassPass and an Alchemy Code Lab graduate (2017). One of the biggest challenges I faced as a new engineer was learning how to pause before coding, plan my work and collaborate with my co-workers.

  Since there aren't any hard-set industry standards for designing software, nor could there be, a common practice is to create a technical document explaining your how you plan to tackle your project.

  Writing TDDs is a skill, and takes practice. It's my belief that starting early in your career will help you learn, grow and advance.

  In this workshop, I'll go over the basics. I'll show you how know when you need a TDD and how to think through your design. I'll share with you some examples and templates for all levels of complexity and difficulty.

  Feel free to contact me at christinelaguardia@gmail.com or connect on [LinkedIn](https://www.linkedin.com/in/christy-la-guardia).
</details>

<details>
  <summary>Presentation</summary>
  View the slides: https://christylaguardia.github.io/tdd-workshop/

  The presentation is written in markdown and converted to html using [Marp](https://marp.app/). See the [Marp docs](https://marpit.marp.app/markdown) for markdown syntax.

  To convert the md to html:

  1. Install the [marp-cli](https://github.com/marp-team/marp-cli) with `brew install marp-cli`.

     ```bash
     brew install marp-cli
     ```

  2. Convert markdown to html

     ```bash
     marp presentation.md -o index.html
     ```
</details>

## Workshop Instructions

Working individually or in pairs, practice writing a TDD!

1. **Choose a project to use as the subject of your TDD.**

   Don’t spend a long time deciding what this is. The project itself isn’t *that* important for this exercise, so it doesn’t need to be unique or special. If you're not sure, start with something simple. It can be a project you’ve already completed or you can come up with an idea.

2. **Select a template.**

   Start with one of the sample templates, in order of complexity + difficulty:

    1. [simple](templates/simple.md)
    2. [practical](templates/practical.md)
    3. [extended](templates/extended.md)
    4. [step-by-step](templates/step-by-step.md)
    5. [phased](templates/phased.md)
    6. [google](templates/google.md)
    7. [comprehensive](templates/comprehensive.md)

    Each template has sections with guidelines on what to write in that section in the comments `<!-- -->`.

    If none of the templates seem right for your project, feel free to copy one and modify the sections, or create your own.

3. **Write your TDD**

    Create a branch. Make a copy of your selected template in the [workshop](/workshop) folder. Work through each section of the template, reading the guidelines comments and writing as you go. Remember, don't overthink everything, write what you know, call out what you don't know.

4. **Create a PR**

    Submit your TDD for peer-review by creating a pull request.

5. **Review other TDDs**

    Find a pull request that needs review. Read through the TDD. Ask questions or leave comments by submitting a [review](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews).

    When reviewing someone's TDD, conider:

    - Do you understand the context?
    - Can you follow the design or implementation details?
    - Is complexity and difficultly explained?
    - Are there areas that could use some more explanation or details?
    - Questions you might have?

## Markdown Tips

1. Skip VS Code, and write and commit your markdown directly in GitHub.
2. Write nicely formatted markdown with the [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) and the [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) extensions for VS Code.

## Resources

- [A Practical Guide to Writing a Software Technical Design Document (by Grace Huang)](https://medium.com/swlh/a-practical-guide-to-writing-a-software-technical-design-document-c6f4d865ccff)
- [A practical guide to writing technical specs (by Zara Cooper, Stackoverflow)](https://stackoverflow.blog/2020/04/06/a-practical-guide-to-writing-technical-specs/)
- [Design Docs at Google (by Malte Ubl, Industrial Empathy)](https://www.industrialempathy.com/posts/design-docs-at-google/)
- [Technical Design (Stanford IT)](https://uit.stanford.edu/pmo/technical-design)
- [Why Tech Specification is Important? (by Slava Podmurnyi, Visartech)](https://www.visartech.com/blog/10-reasons-why-you-should-write-technical-specification/)
- [Writing Technical Design Docs (by Talin, Engineering Insights)](https://medium.com/machine-words/writing-technical-design-docs-71f446e42f2e)
