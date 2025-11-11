---
title: Markdown
subtitle: An easy-to-read, easy-to-write plain text format  
date: 2016-12-29 21:25:54
tags: markdown
---
Markdown is *mostly* used as a **text-to-HTML conversion tool** for web writers. After writing using **plain text format**, your markdown document can be converted to structurally valid XHTML (or HTML). For instance, GitHub uses markdown to preview readme’s. Also the posts on this blog are written in markdown.
<!-- more -->
Markdown can not only be converted to HTML. For instance, RStudio uses R Markdown (a combination of markdown and R code chunks) to publish a report about your R code to Word, PDF, {% katex %}\LaTeX{% endkatex %}, or even a presentation.

The strength of markdown is that a Markdown-formatted document is **publishable as-is**, as plain text, without looking like it’s been marked up with tags or formatting instructions.

## Syntax
---
This section covers the basic syntax of markdown. For more details on the syntax redirect to [daring fireball](https://daringfireball.net/projects/markdown/syntax).

### Block Elements
---
#### Headers
---
There are two header styles, **Setext** and **Atx**.  
Setext headers are marked by underlining, equal signs for first-levek headers and dashes for second-level headers.

    H1
    ==

    H2
    --

H1
==

H2
--

Atx headers are marked with 1–6 hash characters, corresponding to header levels 1-6.


    # H1
    ## H2
    ### H3
    #### H4
    ##### H5
    ###### H6


# H1
## H2
### H3
#### H4
##### H5
###### H6

#### Blockquotes
---
Blockquotes are similar to quoting passages in an email message. Blockquotes are marked with `>`. You can mark every line of the blockquote or just the first line. Blockquotes can also be nested. Markdown syntax in a blockquote is allowed.

    > This is the first level of the quote. 
    As you can see, only the first line needs to be marked with a `>`.
    >> Blockquotes can also be nested. 
    This is the second level of the quote.

> This is the first level of the quote. 
As you can see, only the first line needs to be marked with a `>`.
>> Blockquotes can also be nested. 
This is the second level of the quote.

#### Lists
---
Markdown supports ordered lists, marked with a number following a dot, and unordered lists, marked with a `*`, `+` or `-`. Lists can also be nested with mixed types.

    - item 1 
    - item 2
        1. item 2.1
        2. item 2.2
    - item 3

- item 1 
- item 2
    1. item 2.1
    2. item 2.2
- item 3

#### Code blocks
---
A code block is simply marked with 1 tab or 4 spaces:


    This is a code block


#### Horizontal rules
---
Horizontal rules are marked with 3 or more `*` or `-`:


    -----
    * * *


### Span Elements
---

#### Links
---
There are 2 types of links in markdown, inline links and reference-style links. In both styles, the link text is marked by square brackets and the title attribute is optional. There are two types of paths for each style of links. Absolute paths refering to global resources or relative paths refering to local resources on the same server.

    This is [an example](http://example.com/ "Title") inline link.  
    [This inline link](http://example.net/) has no title attribute.  
    [This inline link](/archive/) refers to a local resource.

This is [an example](http://example.com/ "Title") inline link.  
[This inline link](http://example.net/) has no title attribute.  
[This inline link](/archive/) refers to a local resource.

    This is [an example][1] reference-style link.

    [1]: http://example.com/ "Optional Title Here"

This is [an example][1] reference-style link.

[1]: http://example.com/ "Optional Title Here"



#### Emphasis
--- 
Emphasis is marked by asterisks `*` or underscores `_`. One `*` or `_` marks italic text and two `*`‘s or `_`‘s mark bold text.

    *single asterisks*  
    _single underscores_  
    **double asterisks**  
    __double underscores__

*single asterisks*  
_single underscores_  
**double asterisks**  
__double underscores__


#### Code
---
Use backticks for inline code:

    `print()`

`print()`

#### Images
---
Images are marked exactly the same as [links](#Links), but with an exclamation mark `!` in front.

    ![Markdown](/b-logo-rounded.png)

![Markdown](/b-logo-rounded.png)

### Backslash Escapes
---
Markdown provides backslash escapes for the following characters:


    \   backslash
    `   backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
    +   plus sign
    -   minus sign (hyphen)
    .   dot
    !   exclamation mark


## Installation
---
Markdown is widely accepted by developers and editors. Nearly every popular content management solution supports Markdown, if not out-of-the-box, then with an easy-to-install extension.

### Markdown for Sublime Text
---
**Sublime Text 2/3** can preview and build markdown files quickly in your web browser with the [Markdown Preview](https://packagecontrol.io/packages/Markdown%20Preview) package.

Steps:
1. [Install](https://packagecontrol.io/installation) Package Control if you haven’t yet.
2. Use <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>P</kbd> then select *Package Control: Install Package*.
3. Look for **Markdown Preview** and install it.

### Markdown for Atom
---
**Atom** has the package [Markdown Preview Plus (MPP)](https://atom.io/packages/markdown-preview-plus), which can preview any markdown file with <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>m</kbd>.

Steps:
1. Search for and install `markdown-preview-plus` in Atom’s Settings view.
2. Disable the built-in package `markdown-preview`.
3. *(Optional)* Install and enable Pandoc for citation support.
    