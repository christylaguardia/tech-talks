---
marp: true
---
<!-- class: invert -->

# How to write a Technical Design Document (TDD)

## Christy La Guardia, Senior Software Engineer, ClassPass

<!--
  Pre-start questions:
  - Where are you in the program?
  - What did you do before code school?
  - Have you ever heard of a TDD?
-->

---

# We'll cover...

1. What is it?
2. Why is it needed?
3. How do you know if you need one?
4. How to write one?
5. Practice!

---

# What is a Technical Design Document (TDD)?

## It's a document you will write before building something. It explains and validates your technical decisions and design.

Typically, your engineering team will have a shared understanding of what it is and when to use it, and probably a template. (If not, you can bring it up!)

a.k.a: Software Design Document, Engineering Design Document, Technical Specification

---

# What is a Technical Design Document (TDD)?

---

## Examples

- Creating a new large feature
- Building a new web API
- Implementing widespread design changes
- Major library vision upgrade
- Planning a large refactor
- Burning down tech debt

---

# These **challenging** questions will come up:

- How are you going to build _____?
- How long will it take to build _____?
- Did you think of _____?
- Why did you decide to use _____?
- Is _____ in scope?
- How much work is it to do _____?

<!--
  Notes:
  - Intimidating questions, see them as an opportunity
  - I wasn't prepared for this
  - Made the mistake of way over/under estimating
-->

---

# How a TDD (or TDD-like) process will help you as a new engineer

- Gives you a **structured** approach to taking on a big project and working through hard problems
- Helps you have **confidence** in your design
- Encourages **learning** from other engineers
- Creates an **authoritative** source of truth for what you're building

<!--
  Notes: I had a hard time with developer vs. engineer, and believing I was past entry-level.
  The TDD process was CRITICAL to advancing to Mid and Senior levels.
-->

---

# How I felt about TDDs

- I don’t know what this is.
- I’m not qualified, this is a job for a senior engineer.
- I don’t build anything that complex.
- I don’t even know where to start.

![bg right:40% 80%](https://media.giphy.com/media/cLJdDcAWTkW6k/giphy.gif)

<!--
  Notes: Felt like something I had to get over with so I could get to coding.
-->

---

# How I now feel about TDDs

- I understand what a TDD is, and how to use it effectively.
- This process can be followed by engineers at all levels, it’s a skill to be developed.
- Even with simple tasks, a structured design process can speed up the implementation process and avoid reworks.
- I know how to get started!

![bg right:40% 80%](https://media.giphy.com/media/YFis3URdQJ6qA/giphy.gif)

<!--
  Notes: It's a tool I keep in my back pocket.
-->

---

# Advantages of writing a TDD

- Forces you to examine a problem (*before* coding)
- Identifies missing requirements
- Helps the team collaborate
- Ship faster
- Prevents scope creep
- Helps resolve problems that pop up later
- Serves as documentation
- Saves time & money!

---

# Disadvantages of writing a TDD

- Upfront cost (time)

---

# Getting Started

---

# When do you need a TDD?

- No industry standard or hard-and-fast rules
- Your team should set the prerequisite criteria (doesn't including finalized product or design requirements)
- You should carefully weigh the cost vs. benefit

---

# From the ClassPass docs:

*Any project that we estimate will take more than 2 weeks for one engineer to complete requires a TDD and getting feedback from the engineering team.*

---

<!-- How to draw an owl meme -->
![bg contain](https://i.imgur.com/rCr9A.png)

---

<!-- Kids guide to drawing an owl-->
![bg contain](https://artprojectsforkids.org/wp-content/uploads/2021/10/How-to-Draw-an-Owl-Face-diagram.jpg)
<!-- Source: [Easy How to Draw an Owl Face Tutorial and Owl Face Coloring Page](https://artprojectsforkids.org/how-to-draw-an-owl-face/) -->

---

<!-- Difficulty and complexity diagram -->
![bg contain](https://www.projecttimes.com/wp-content/themes/yootheme/cache/ad0145173c00f7fe99af7442fbe6a818-a6198ff7.jpeg)
<!-- Source: [A Simplified Approach To Determine IT Project Complexity](https://www.projecttimes.com/articles/a-simplified-approach-to-determine-it-project-complexity/) -->

---

# Factors to consider when deciding to write a TDD

1. Size
1. Complexity
1. Uncertainty
1. Dependencies

---

# 1. Size

What is the amount work?
How long will it take?
How many engineers?
1 day?
1 week?
1 month?
Have no idea?

---

# 2. Complexity

Lots of logic?
Business rules or logic?
Intricate UI?
A new server or service?
Data changes or big database migrations?

---

# 3. Uncertainty

Introducing a new technology or library?
Language or framework the team is unfamiliar with?
How will these changes rollout?
Known issues or tech debt?

---

# 4. Dependencies

## Internal

Will this be used by another team?
Will this impact another team’s system?

## External

Adding a new vendor?
What are the costs?
What are the maintenance costs?

---

# Still not sure?

Consider doing some research, exploratory work or a spike with the goal to gather information in order to make a decision on the path forward.

(See the [discovery template](templates/discovery.md).)

---

# Example 1

You have been asked to add a “Get in touch” button to an existing web page.
When clicked, this button will open up the the existing “Contact Us” page in a new window.

*Size? Complexity? Uncertainty? Dependencies? . . . Should you write a TDD?*

<!--
  Notes:
  - Size: How much? How long? How many people?
  - Complexity: Logic? Rules? UI? New thing? Data?
  - Uncertainty: New tech? Familiarity? Known issues?
  - Dependencies: Used internally? New dependencies?
-->

---

# Example 2

In addition, you’ve been asked to add a form to the “Contact Us” page, so that the user can submit their message without using email.

*Size? Complexity? Uncertainty? Dependencies? . . . Should you write a TDD?*

<!--
  Notes:
  - Size: How much? How long? How many people?
  - Complexity: Logic? Rules? UI? New thing? Data?
  - Uncertainty: New tech? Familiarity? Known issues?
  - Dependencies: Used internally? New dependencies?
-->

---

# Example 3

To allow the customer service team to reply to the “Contact Us” messages, they should be distributed evenly to customer service representatives. Ensure that messages are replied to in the order received and priority. Customer service team managers should be able to view all incoming and outgoing messages, and the messages assigned to each representatives. Also, we’d like to see a dashboard with a summary of total messages received and sent, so we can monitor work load and track growth.

*Size? Complexity? Uncertainty? Dependencies? . . . Should you write a TDD?*

<!--
  Notes:
  - Size: How much? How long? How many people?
  - Complexity: Logic? Rules? UI? New thing? Data?
  - Uncertainty: New tech? Familiarity? Known issues?
  - Dependencies: Used internally? New dependencies?
-->

---

# Sections of the TDD

1. Explain
2. Plan
3. Decide

<!-- Notes: This is a high-level overview, each template has a different structure. -->

---

# 1. Explain

## Introduction, Context, Problem/Solution, Goals/Non-Goals

What problem are you trying to solve?
Why does it need to be solved? What is the impact?
What are the goals of this project?
What contextual or background information should the reader know?

---

# 2. Plan

## Technical Approach, Considerations, Phases/Steps

How are you going to solve the problem?
What are the technical implementation details?
What factors are relevant or need special consideration?

---

# 3. Decide

## Options, Alternatives, Release

What is the time and effort to implement?
Are there alternatives? What are the costs?
Any future work? Maintenance?

---

# Other TDD Tips

---

# Estimating *Level of Effort* (LOE) using T-Shirt sizes

Using T-Shirt sizes to give estimates of LOE is really helpful when you can’t give exact estimates.

Size | Example Time Estimate
-- | --
XS | 1 or 2 days
S | 1 week
M | 2 weeks
L | 4 weeks
XL | Anything more

---

# Consider your audience

- Fellow engineers
- Engineering managers
- Product manager?
- Designers?
- Project mangers?
- Stakeholders?

---

# Proofreading

- Look for unfounded assumptions ("This always works." "This will be easy.")
- Edit subjective words ("I feel", "I think", "Good/bad")
- Make sure it sounds professional (No "hey guys")
- Use correct spelling and grammar

---

# Reviewing and commenting

1. Decide who to share it with
2. Ask feedback & reviews
3. May want to lead a meeting
4. Reply to comments, answer questions
5. Revise your TDD
6. Consider keeping it updated or additional docs
7. Make a decision and start coding!

---

# Examples

- [Simple](/templates/simple-example.md)
- [Practical](/templates/practical-example.md)