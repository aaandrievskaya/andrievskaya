---
title: Markdown language.
subtitle: Learn how to write reports using the lightweight Markdown language


# Summary for listings and search engines
summary: Learn how to write reports using the lightweight Markdown language

# Link this post to the project
projects: []

# Date published
date: '2022-05-14'


# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false


authors:
  - admin
  - Andrievskaya A.A.

tags:
  - Work
  - Markdown 

categories:
  - Demo
---

## Definition

Markdown is a simple markup language used to create rich text (such as HTML) with a text editor. It allows you to add basic formatting to text using characters known and available on all keyboards. Font size, color, and other advanced options are not available in Markdown.

## Markdown Syntax

This is a quick reference to the basic elements of Markdown syntax. There is no single standard, and different versions of Markdown may differ in details. But the basic elements from the list below are supported in all standards.

## Text selection
*This text will be italicized*
_This text will be italic (italic)_

**This text will be bold**
__This text will be bold__

_You can **insert** one type into another_

## Titles

'# This is the largest heading, it turns into an <h1> tag
'## <h2>
'### <h3>
'#### <h4>
'##### <h5>
'###### <h6>

In Markdown, headings are written without the symbol '

## Links
https://hexlet.io - the text of a simple link will become a clickable link automatically
You can make any text a link:

[This is a Hexlet link](https://hexlet.io)

## Quote

>That's a wise quote
> wise man.

## Pictures

![This is optional alt text](/assets/images/markdown/markdown.png)

## The code

To highlight code (or any unformatted text), special characters are used - back ticks: `

Sometimes you need to add a piece of code `function(12);` to a regular line of text.
And sometimes you need to insert a whole block of code:

```javascript
const func = (num) => {
  if (num > 0) {
    return num - 1;
  }
  return num + 1;
};
```

## Lists

Unnumbered list:

* Paragraph
*One more item
  * Subparagraph
  * Another sub-item
Numbered list:

1. Item
1. One more point
  1. Subparagraph
  1. One more subparagraph
You can use any numbers in a numbered list - it doesn't matter. When converted to HTML or another format, the numbers will become correct and consistent (1, 2, 3, etc.).

