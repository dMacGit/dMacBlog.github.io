---
title: 'HTML Cheat Sheet'
date: 2019-06-20
permalink: /posts/2019/06/20/Html-Cheat-Sheet/


tags:
  - Html
  - Web Development
  - Websites
  - Cheat Sheet
---

# **HTML Cheat Sheet**

**Note:**
_Content refferenced from:_
[developer.mozilla.org](developer.mozilla.org).

_Do check it out. It's one of the best sources for learning HTML_

---

## **The Basics:**

### First thing to know is page structure.

**HTML Element**

``` html
<html></html>
```
The html element represents the root or Top-level element of an html document. 
This is also reffered to as the root element. **ALL** other elements must be decendence of this element.
This follows the ```<head>``` element.

**Main Body Element**

``` html
<body></body>
```

This is the main Element that represnets the content of an HTML document.
There can only be _ONE_ ```<body>``` element.
This is contained in the ```<html>``` element.

**Content Division Element**

``` html
<div></div>
```

General purpose container for how the content flows on the page. 
Used to help layout the structure of the page when combined with CSS styles
There can be any number of ```<div>``` elements in the document.
This must be contained inside the ```<body>``` element.

### Next is how to display text/content.

**Headings Element**

``` html
<h1>Heading 1 text</h1>
```
# Heading 1 text

``` html
<h2>Heading 2 text</h2>
```
## Heading 2 text

``` html
<h3>Heading 3 text</h3>
```
### Heading 3 text

``` html
<h4>Heading 4 text</h4>
```
#### Heading 4 text

``` html
<h5>Heading 5 text</h5>
```
##### Heading 5 text

``` html
<h6>Heading 6 text</h6>
```
###### Heading 6 text

```<h1>``` to ```<h6>``` elements represent 6 levels of section headings.
From ```<h1>``` (Largest) to ```<h6>``` (Smallest)

**Pharagraph Container**

``` html
<p>"Some text"</p>
```
"Some Text"

Represents the Paragraph element. 
Paragraphs can contain text blocks, by blank lines or grouping related content like images and forms

**Code Container**

``` html
<pre><code>"Hello World!"</code></pre>
```
"Hello World!"

Displaying blocks of code. Used to tell document renderer that this block with contain code, and to render/output accordingly