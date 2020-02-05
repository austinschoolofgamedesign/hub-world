# How to contribute to the *Austin School of Game Design*

- organizing though consistent folders and filenames
- What tags are best to start with?
- Short Links to Important Resources:
  - docs: handbook / roadmap (you'll learn more about this in the roadmapping session)
  - bugs: issue tracker / bug report tool
  - comms: forum link, developer list, IRC/email
<!-- todo: finish this list -->

## A Big Welcome

We're *so* glad you're here!
The *Austin School of Game Design* is a large ongoing project that is trying to do the work of many full-time employees, without the employees.
For that to be possible, we thrive off of contributions from awesome peoplel like you.

If this is your first time contributing to an open source project, then read on!
We have detailed instructions so you don't get overwhelmed by it all.
There's some technical jargon you'll need to pick up on, but it's nothing too bad once it's all explained.

If you're a hardened open source veteran, then you'll find that contributing to a non-software open source project is a tad different than contributing to its software counterparts.
It's not *dramatically* different, but the purposes and organization are more fluid.
Expect more discussion and soft opinions here.

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
1. [Join the Conversation](#join-the-conversation)
1. [How to Use GitHub](#how-to-use-github)
1. [Formatting and Styling](#formatting-and-styling)
1. [Folder and File Naming](#folder-and-file-naming)
1. [When You're Ready to Submit](#when-youre-ready-to-submit)

## Code of Conduct

Before we get to the fun stuff, we need to set some ground rules.
We're all part of a larger community here, and we all want the same end goal - to build the best and most accessible game design school in the world.
However, sometimes we have different opinions about the steps to get there, and tensions can get high.
So we've put together some basic ground rules to make sure that everyone can work together amicably.

Before going further, take some time to read through the [**Code of Conduct**](/CODE_OF_CONDUCT.md).
Let's all do our part to make sure this place is an awesome place to share our thoughts and feels about games.

## Join the Conversation

Now that the ground rules are out of the way, it's time for us to get to know each other.
We have two official places set up to talk. Both places are great for getting to know other game design nerds.

1. The first is in the [Issues](https://github.com/austinschoolofgamedesign/hub-world/issues)  section of GitHub.
When you have an idea of something you want to contribute, open up an Issue and start a conversation.
1. For less formal conversations, jump into the [*Austin School of Game Design* Discord channel](https://discord.gg/mbPRNRG).
We're always happy to see new faces and learn what brought you our way.

## How to Use GitHub

There's a lot of jargon around GitHub that will take some getting used to if you're not familiar with it.
In this section we'll go over some of the common terms and how we use them at *ASGD*.

> ### If you already know how to use GitHub (TL;DR):
>
> *ASGD* uses [**Issues**](https://github.com/austinschoolofgamedesign/hub-world/issues) as the place for permanent discussion, as well as for making suggestions for updates, requests and typo fixes.
> Think of Issues as the *ASGD* forums with a focus on making content rather than being a discussion archive.
>
> [**Pull Requests**](https://github.com/austinschoolofgamedesign/hub-world/pulls) are where we keep all new content.
> As soon as you start working on something new, make a new branch and open a 'Draft Pull Request'

<!-- todo -->

### Start conversations by creating an 'Issue'

<!-- todo -->

### Work In Progress (WIP) goes in a 'Pull Request'

<!-- todo -->

## Formatting and Styling

Everything here is written in plain-text using Markdown for formatting.
This may take a bit of getting used to at first, but we've got you covered.

If you're a software developer, there are some fantastic Markdown tools built into your IDE.
If you're not comfortable using the dev tools, I recommend checking out free Markdown editors like [Dillinger](https://dillinger.io/).

### Brief overview of Markdown

Modern word processors like Microsoft Word or Libre Office have a ton of options for styling text with different fonts, colors and layouts.
For our purposes at *ASGD*, most of those features only cause problems.
Markdown simplifies the process by removing all but the essential styling options, and asks you to type them out manually in plain text.
When first using Markdown, it feels a little messy, especially when you don;t remeber what the different symbols mean.
But a day of practice soves that problem.

There is a ton of really helpful documentation of how Markdown works.
Rather than trying to reinvent the wheel here, I recommend you go check out these two links:

- [Markdown Basic Syntax](https://www.markdownguide.org/basic-syntax/) - Start here
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/) - Use this once you get the hang of it

Here's an example.
I can write this:

```markdown
**Welcome to *ASGD*!**

This is a [link to Google](www.google.com).

- And here's a list

1. And a numbered list
1. A second number
```

And the output is:

> **Welcome to *ASGD*!**
>
> This is a [link to Google](www.google.com).
>
> - And here's a list
>
> 1. And a numbered list
> 1. A second number

From a programming and publishing perspective, the main reason we use Markdown is because it plays very nicely with the internet, eBooks and traditional publishing.
No additional formatting and style changes need to be made before submitting a document for final presentation.
Since we're a community of volunteers, less work before presentation means more visibility (and therefore hopefully adoption).

### *ASGD* Styling Conventions

Now that you've got an idea of what Markdown is, and the simplified styling it provides, let's take a look at how we use the different styling options.

| **Markdown** | **Name** | ***ASGD* Usage** |
|-----------------|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| `#` | Main Header | There is only one of these in the entire document. It's pulled by the computer to generate the title of the article. |
| `##` - `######` | Additional Headers | All additional header levels are automatically pulled for generating a 'Table of Contents' for easier navigation |
| `*text*` | Italic and Bold | We use the `*` symbol to surround words for italics and bold. Not the `_` symbol. |
| `-` | List | Lists are started with the `-` symbol. |
| `⮐` | Line Break | This is a weird one, but still important. We make a new line after every single sentence. Markdown will render the text as one large paragraph, but the data is stored on multiple lines. This convention helps track changes to articles over time. |

GitHub tracks changes to all documents across time, along with the person that made those changes.
But it can only keep track of that on a line by line basis.
So by breaking paragraphs into individual lines, we allow GitHub to track changes on a sentence by sentence basis, rather than a paragraph basis.

A double line break is used instead of a single line break to create new paragraphs.

And in case you were wondering, the above two paragraphs look like this behind the scenes:

```markdown
GitHub tracks changes to all documents across time, along with the person that made those changes.
But it can only keep track of that on a line by line basis.
So by breaking paragraphs into individual lines, we allow GitHub to track changes on a sentence by sentence basis, rather than a paragraph basis.

A double line break is used instead of a single line break to create new paragraphs.
```

## Folder and File Naming

### Filenames

Because *ASGD* has a lot of files across many different kinds of discussions, we use a simple but strict naming convention to make sure everything is accounted for.

Here are a few examples of possible filenames:

- `202002041148-dekuTreeAnalysis.md`
- `201912312013-responseToChartDependencies.md`
- `202106131347-nierAutomataMenu.jpg`

There are three required elements to each filename.

- Unique ID timestamp followed by a hyphen
  - Every filename starts with a timestamp following the convention `YYYYMMDDhhmm`, using the 24hr convention for the hours.
  For convenience sake, use the current time displayed on your computer's clock.
  For example, If I were to create a timestamp for right now it would be `202002041144` which is the year 2020, month 02, day 04, hour 11, minute 44 - **11:44 am, February 4th, 2020**.
  This is a simple way to create meaningful and consistently lengthed unique IDs for each file without needing to use a third party tool.
  - The timestamp is to make the file computer readable.
  Even if the description is the same, the computer can differentiate between the files because of the unique ID.
- Camel case file description
  - The actual description is to make the filename human readable.
  Something short and descriptive is best.
  - Camel case naming is a programming convention that removes the need to add spaces between words when it's part of a filename or variable.
  The first word is lower-case, and each word following is capitalized.
  For example, if I analyzed the Deku Tree from *Ocarina of Time*, I might want to call it '*Deku Tree Analysis*'.
  To convert it to camel case, I would remove the spaces and lower-case the first word - `dekuTreeAnalysis`.
- The file extension
  - Because modern operating systems default to automatically adding filenames to the end of your files, it's easy to forget to add it manually.
  Specifically be careful to always remember the `.md` extension for Markdown text files.
  The computer uses the `.md` extension to format the text correctly.

### Folders

<!-- todo -->

## When You're Ready to Submit

<!-- todo - How to do a 'Merge/Squash' -->