---
title: 'Changing Jekyll Rouge Code Font Size'
date: 2019-06-25
permalink: /posts/2019/06/25/Jekyll-Rouge-Font-Size/

tags:
  - Rouge
  - Jekyll
  - Markdown
  - Blog
  - General
---

## How to change Rouge Font size in Jekyll

In order to change the font size of code highlighting in Jekyll, there are a few places to modify.

The easiest place to change, is in the **_syntax.scss** file under **/_sass** folder in the root directory.

In the ```div.highlighter-rouge, figure.highlight {}``` block, under ```.highlight{}``` simply change the ```font-size``` value.

shown here:

``` scss
div.highlighter-rouge, figure.highlight {
    position: relative;
    margin-bottom: 1em;
    // Skipping lines for compactness
    &:before {
        //Skipping more lines
    }

    .highlight 
    {
        margin: 0;
        font-family: $monospace;
        font-size: $type-size-7; //<-- This line here
        line-height: 1.8;
    }
}
```

You can override the default size, by tweaking the em value.
For my purpose **.85em** of **16px** size, makes the code slightly larger and more readable.

``` scss
.highlight 
{
    margin: 0;
    font-family: $monospace;
    font-size: 0.85em; //Overriding default
    line-height: 1.8;
}
```

The other way you can tweak the font-size is from in the **_variables.scss** file in the same **/_sass** folder.

In this file is where the global variables are located, includeing (for this theme) the varying sizes of defined font types.

Code highlighting in the **_syntax.scss** file was set to ```$type-size-7```. So modifying the **em** value of that variable here would change any element mapped to this font size type-number.

``` scss
/* type scale */
$type-size-1                : 2.441em;  // ~39.056px
$type-size-2                : 1.953em;  // ~31.248px
$type-size-3                : 1.563em;  // ~25.008px
$type-size-4                : 1.25em;   // ~20px
$type-size-5                : 1em;      // ~16px
$type-size-6                : 0.75em;   // ~12px
$type-size-7                : 0.6875em; // ~11px
$type-size-8                : 0.625em;  // ~10px
```