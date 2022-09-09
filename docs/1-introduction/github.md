---
sidebar_position: 3
---

# D1S3. Introduction to GitHub

[Slides](https://hackmd.io/@D3o17PKxQImUPBfYYD6wYg/HkmgpO5l5#/2/0/0)

[GitHub](https://github.com/) is an online service that developers use to store their code and to collaborate.

GitHub has a range of useful features:

- Issues and Projects for project planning
- Pull Requests for data analysts and coders to merge comtributions from different team members into a single codebase
- Insights to measure contributions from different team members
- Actions to automate pipelines
- Options to review each other's code

## Some noteworthy GitHubs

### [Linus Torvalds](https://github.com/torvalds)

The green dots on a profile page show contributions. The creator of Linux contributes to his six reposiories almost every day.

The repository for Linux was starred a lot.

![](https://i.imgur.com/BhP6P35.png)

### [A good data repository](https://github.com/n-gao/gapminder)

Have a look around [this repository](https://github.com/n-gao/gapminder). It is a data project that recreates [Hans Rosling's](https://en.wikipedia.org/wiki/Hans_Rosling) Wealth and Health visualization.

In the toop right corner you can find a published app, in the codebase some `.csv` files with data.

The reposiory is well documented with a README.

If you navigate to the owner's profile you will also find a pinned repo with Jupyter notebook research and a link to a published paper.

## Markdown

Markdown is a very simple computer language.
It is not sophisticated enough to build apps,
but it is easily the best way to style text on the web.
There are several flavours of the Markdown language.
The one we focus on is known as the [GitHub flavour](https://guides.github.com/features/mastering-markdown/).

## Styling with Markdown

### Headers

You can add headers to the article using the format below.
> ⚠️ There **_must_** be a space between the first word and the last hash
or pound sign.

```markdown
# H1 - use one hashtag to make the top level header
## H2
### H3
#### H4
##### H5
```

### Emphasis

Add emphasis to the article using the format below

- Emphasis, aka italics, with `*asterisks*` or `_underscores_`
  - *asterisks* or _underscores_
- Strong emphasis, aka bold, with `**asterisks**` or `__underscores__`
  - **asterisks** or __underscores__
- Combined emphasis with `**asterisks and _underscores_**`
  - **asterisks and _underscores_**
- Strikethrough uses two tildes `~~Scratch this~~`
  - ~~Scratch this~~

### Blockquotes

Add quotes to the article using the format below:

``` markdown
> Add the angle bracket `>` to add an indent to the quote in the article
```

> Add the angle bracket `>` to add an indent to the quote in the article

```markdown
> Quotes spread one line apart
> will be shown in the same quote
```

> Quotes spread one line apart
> will be shown in the same quote

### Lists

To produce numbered lists add a number (any numbers would work,
but all 1s are common) followed by a dot and a space
at the start of the line:

```markdown
1. Numbers create
1. An ordered list
1. In the article
```

1. Numbers create
1. An ordered list
1. In the article

<!-- markdownlint-disable MD004 -->

```markdown
* Unordered lists can use asterisks
- Or minuses
+ Or pluses
```

* Unordered lists can use asterisks
- Or minuses
+ Or pluses

<!-- markdownlint-enable MD004 -->

To create a nested list add two spaces to its starting position.

```markdown
- The first line
  - The indented line
- The next line
```

- The first line
  - The indented line
- The next line

## Adding inline elements to posts with Markdown

### Images

You can add an image to the markdown body using the format below

```markdown
![alt text](file URL)
```

For example, to include this image

![Image example](/img/icons/github-logo.svg)

the following markdown was used:

```markdown
![Deepnote logo](/img/icons/github-logo.svg)
```

### Hyperlinks

Add hyperlinks to the text body using the format below

```markdown
[I'm a link to Google](https://www.google.com)
```

[I'm a link to Google](https://www.google.com)

## Making slides with Markdown

The best way to learn Markdown is to write in Markdown. There is an app that allows making slide decks using Markdown. It is called Hackmd. Please sign up with your GitHub account.

[Link to hackmd](https://hackmd.io/)

Hackmd is very intuitive, and you can switch between typing Markdown and using its GUI. To make a new slide use `---`:

<img
  src="/img/day-1/hackmd-intro.png"
  alt="Hackmd"
  class="wide screenshot"
/>

To turn your Markdown document into slides, change the mode and choose to preview:

<img
  src="/img/day-1/slide-mode.png"
  alt="Hackmd"
  class="narrow screenshot"
/>