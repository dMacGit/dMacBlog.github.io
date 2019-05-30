---
title: 'Documenting code in Markdown'
date: 2019-05-30
permalink: /posts/2019/05/30/Markdown-and-Code/

tags:
  - Development
  - Project
  - Git
  - Github
  - Markdown
  - Linux
---

# Markdown basics

Here is a quick quide on some basics in markdown for particular situations when writing up documentation.

## Code syntax

For when you want to document code within a markdown page you can do so in a couple of ways.

#### Block-quotes

For situations where only a single line is the focus, and code/syntax highlighting isn't required, block-quotes can be handy.
Block quotes only require a starting '>' character, and the code follows.
The block is closed by leaving a blank line after the end of the code.

``` markdown 
> code goes here!
```

#### Fenced code blocks

For multi-line code segments with syntax highlighting, you can use back-ticks to surround a code section.
Three (3) back-ticks start and stop the code section '```' :

````

``` javascript
function start()
{ 
    console.log("Hello World");
}

```
````

To define what code is being shown, write the language trailing the starting back-ticks.
A supported list on what languages are supported by code highlighting by github markdown can be seen [here](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)

